---
UID: NF:certbcli.CertSrvBackupFree
title: CertSrvBackupFree function (certbcli.h)
author: windows-sdk-content
description: Used to free memory allocated from certain Certificate Services Backup APIs.
old-location: security\certsrvbackupfree.htm
tech.root: SecCrypto
ms.assetid: dbfac3fc-3156-4253-812a-8b0647719096
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertSrvBackupFree, CertSrvBackupFree function [Security], _certsrv_certsrvbackupfree, certbcli/CertSrvBackupFree, security.certsrvbackupfree
ms.topic: function
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certadm.dll
api_name:
 - CertSrvBackupFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertSrvBackupFree function


## -description


The <b>CertSrvBackupFree</b> function is used to free memory allocated from certain Certificate Services Backup APIs.


## -parameters




### -param pv [in]

A pointer to the memory to be freed.


## -returns



This function does not return a value.




## -remarks



Call this function when finished with memory allocated by using the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/bbc6e6c2-bb2c-4b0e-b1ba-6acf26a48f45">CertSrvBackupGetBackupLogs</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e62be79-693a-4543-8d83-262f00686c99">CertSrvBackupGetDatabaseNames</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ff60b705-5ac6-4e61-9b88-9ffc2dc9adce">CertSrvBackupGetDynamicFileList</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6f32e7f4-60d5-4370-b240-46aa2475e279">CertSrvServerControl</a>
</li>
<li>
<a href="https://msdn.microsoft.com/02355bd7-6788-4c32-940e-b89e47619aa0">CertSrvRestoreGetDatabaseLocations</a>
</li>
</ul>

#### Examples


```cpp
FNCERTSRVBACKUPFREE* pfnBackupFree;

char * szBackupFreeFunc = "CertSrvBackupFree";

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnBackupFree = (FNCERTSRVBACKUPFREE*)GetProcAddress(hInst,
                      szBackupFreeFunc);
if ( NULL == pfnBackupFree )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackupFreeFunc,
           GetLastError() );
    exit(1);
}

// Use the backup APIs.
// ...

// Free allocated memory.
// pBuff was allocated by another certsrv backup function.
pfnBackupFree(pBuff);
```





## -see-also




<a href="https://msdn.microsoft.com/bbc6e6c2-bb2c-4b0e-b1ba-6acf26a48f45">CertSrvBackupGetBackupLogs</a>



<a href="https://msdn.microsoft.com/5e62be79-693a-4543-8d83-262f00686c99">CertSrvBackupGetDatabaseNames</a>



<a href="https://msdn.microsoft.com/ff60b705-5ac6-4e61-9b88-9ffc2dc9adce">CertSrvBackupGetDynamicFileList</a>



<a href="https://msdn.microsoft.com/02355bd7-6788-4c32-940e-b89e47619aa0">CertSrvRestoreGetDatabaseLocations</a>



<a href="https://msdn.microsoft.com/6f32e7f4-60d5-4370-b240-46aa2475e279">CertSrvServerControl</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

