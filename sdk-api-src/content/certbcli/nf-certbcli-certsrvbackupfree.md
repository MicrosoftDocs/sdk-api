---
UID: NF:certbcli.CertSrvBackupFree
title: CertSrvBackupFree function (certbcli.h)
description: Used to free memory allocated from certain Certificate Services Backup APIs.
helpviewer_keywords: ["CertSrvBackupFree","CertSrvBackupFree function [Security]","_certsrv_certsrvbackupfree","certbcli/CertSrvBackupFree","security.certsrvbackupfree"]
old-location: security\certsrvbackupfree.htm
tech.root: security
ms.assetid: dbfac3fc-3156-4253-812a-8b0647719096
ms.date: 12/05/2018
ms.keywords: CertSrvBackupFree, CertSrvBackupFree function [Security], _certsrv_certsrvbackupfree, certbcli/CertSrvBackupFree, security.certsrvbackupfree
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertSrvBackupFree
 - certbcli/CertSrvBackupFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certadm.dll
api_name:
 - CertSrvBackupFree
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
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetbackuplogsw">CertSrvBackupGetBackupLogs</a>
</li>
<li>
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw">CertSrvBackupGetDatabaseNames</a>
</li>
<li>
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw">CertSrvBackupGetDynamicFileList</a>
</li>
<li>
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvservercontrolw">CertSrvServerControl</a>
</li>
<li>
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw">CertSrvRestoreGetDatabaseLocations</a>
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

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetbackuplogsw">CertSrvBackupGetBackupLogs</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw">CertSrvBackupGetDatabaseNames</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw">CertSrvBackupGetDynamicFileList</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw">CertSrvRestoreGetDatabaseLocations</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvservercontrolw">CertSrvServerControl</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>