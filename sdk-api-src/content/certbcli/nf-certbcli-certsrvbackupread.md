---
UID: NF:certbcli.CertSrvBackupRead
title: CertSrvBackupRead function (certbcli.h)
description: Reads bytes from a Certificate Services file.
helpviewer_keywords: ["CertSrvBackupRead","CertSrvBackupRead function [Security]","_certsrv_certsrvbackupread","certbcli/CertSrvBackupRead","security.certsrvbackupread"]
old-location: security\certsrvbackupread.htm
tech.root: security
ms.assetid: cfc72002-40ee-4854-a026-b956acd5d758
ms.date: 12/05/2018
ms.keywords: CertSrvBackupRead, CertSrvBackupRead function [Security], _certsrv_certsrvbackupread, certbcli/CertSrvBackupRead, security.certsrvbackupread
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
 - CertSrvBackupRead
 - certbcli/CertSrvBackupRead
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
 - CertSrvBackupRead
---

# CertSrvBackupRead function


## -description

The <b>CertSrvBackupRead</b> function reads bytes from a Certificate Services file.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup context.

### -param pvBuffer [out]

Void pointer to storage which will contain bytes read from the file being backed up.

### -param cbBuffer [in]

Size of the storage area referenced by <i>pvBuffer</i>.

### -param pcbRead [out]

A pointer to a <b>DWORD</b> value which represents the actual number of bytes read by <b>CertSrvBackupRead</b>. The number of bytes read can be less than the size of the storage area allocated to <i>pvBuffer</i> if the end of the file has been reached.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

After opening the file for backup purposes (using 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a>), call <b>CertSrvBackupRead</b> to retrieve the contents of the file, and call an application-specific routine to write the contents to a backup medium. <b>CertSrvBackupRead</b> and the application-specific routine can be placed in a loop until all the bytes of the file are read and backed up. When done reading the file, close it by calling 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupclose">CertSrvBackupClose</a>.


#### Examples


```cpp

#include <windows.h>
#include <stdio.h>
#include <Certbcli.h>

#define BUFFSIZE 524288

FNCERTSRVBACKUPREAD* pfnRead;
char * szBackupReadFunc = "CertSrvBackupRead";
BYTE       ReadBuff[BUFFSIZE];
DWORD      cbRead=0;
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnRead = (FNCERTSRVBACKUPREAD*)GetProcAddress(hInst,
                                          szBackupReadFunc);
if ( NULL == pfnRead )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackupReadFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Read the file.
// hCSBC represents an HCSBC used in
// an earlier call to CertSrvBackupOpenFile.
// To read the entire file, this code
// would be placed in a loop.
hr = pfnRead( hCSBC,
              &ReadBuff,
              BUFFSIZE,
              &cbRead );
if (FAILED(hr))
{
    printf("Failed pfnRead call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}

// Use the bytes read as needed. For example,
// in an application-specific routine to back
// up the file contents.
// ...
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupclose">CertSrvBackupClose</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>