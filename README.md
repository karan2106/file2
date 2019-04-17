# file2
#include<stdio.h> #include<pthread.h> intallo[10]; intmax[10]; intneed[10]; intflag; intfl; inti,j,k,p,b,n,r,g,cnt=0,id,newr; intavail[10],seq[10]; void*thread1(); void*thread2(); pthread_mutex_tl,ll; intmain(){ pthread_tt1; pthread_mutex_init(&l,NULL); pthread_mutex_init(&ll,NULL); printf("Enternumberofprocesses"); scanf("%d",&n); printf("Enternumberofresources");
scanf("%d",&r); for(i=0;i<n;i++){ printf("Enterdetailsofp%d",i); printf("\nenterallocation\t"); for(j=0;j<r;j++) scanf("%d",&allo[j]); printf("\nEntermax\t\t"); for(j=0;j<r;j++) scanf("%d",&max[j]); flag=0; } printf("\nEnterAvailableresources\t"); for(i=0;i<r;i++) scanf("%d",&avail[i]); pthread_create(&t1,NULL,thread1,NULL); pthread_join(t1,NULL); printf("\nSystemisinsafestate"); printf("\nThesafeseqis-("); for(i=0;i<fl;i++) printf("p%d",seq[i]); printf(")");
} void*thread1(){ pthread_mutex_lock(&l); pthread_tt2; printf("\nEnternewRequestdetails"); printf("\nENterpid\t"); scanf("%d",&id);
printf("\nEnterrequestforresource\t"); for(i=0;i<r;i++){ scanf("%d",&newr); allo[i]+=newr; avail[i]=avail[i]-newr; } for(i=0;i<n;i++){ for(j=0;j<r;j++){ need[j]=max[i]-allo[j]; if(need[j]<n) need[j]=0; } } cnt=0; fl=0; while(cnt!=n){ g=0; for(j=0;j<n;j++){ if(flag=0){ b=0; for(p=0;p<r;p++){ if(avail[p]>=need[p]) b=b+1; else b=b-1; if(b==r){ printf("\np%disvisited"); seq[fl++]=j;
flag=1; for(k=0;k<r;k++) avail[k]=avail[k]+allo[k]; cnt=cnt+1; printf("("); for(k=0;k<r;k++) printf("%3d",avail[k]); printf(")"); g=1;
}
}
}
} if(g==0){ printf("\requestnotgranted-Deadlockoccured")
