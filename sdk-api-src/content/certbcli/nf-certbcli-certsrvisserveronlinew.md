---
UID: NF:certbcli.CertSrvIsServerOnlineW
title: CertSrvIsServerOnlineW function (certbcli.h)
description: Determines if a Certificate Services server is online; if the Certificate Services server is not online, backup operations will not be successful.
helpviewer_keywords: ["CertSrvIsServerOnline","CertSrvIsServerOnline function [Security]","CertSrvIsServerOnlineW","_certsrv_certsrvisserveronline","certbcli/CertSrvIsServerOnline","certbcli/CertSrvIsServerOnlineW","security.certsrvisserveronline"]
old-location: security\certsrvisserveronline.htm
tech.root: security
ms.assetid: fce1ea87-6c02-433e-af38-99b33528b1f1
ms.date: 12/05/2018
ms.keywords: CertSrvIsServerOnline, CertSrvIsServerOnline function [Security], CertSrvIsServerOnlineW, _certsrv_certsrvisserveronline, certbcli/CertSrvIsServerOnline, certbcli/CertSrvIsServerOnlineW, security.certsrvisserveronline
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvIsServerOnlineW (Unicode)
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
 - CertSrvIsServerOnlineW
 - certbcli/CertSrvIsServerOnlineW
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
 - CertSrvIsServerOnline
 - CertSrvIsServerOnlineW
---

# CertSrvIsServerOnlineW function


## -description

The <b>CertSrvIsServerOnline</b> function  determines if a Certificate Services server is online; if the Certificate Services server is not online, backup operations will not be successful.

## -parameters

### -param pwszServerName [in]

A pointer to the NetBIOS or DNS machine name of the server to check for online status.

### -param pfServerOnline [out]

A pointer to Boolean value which will be <b>TRUE</b> if the Certificate Services server is online and <b>FALSE</b> if it is not online.

## -returns

The return value is an <b>HRESULT</b>. This function will fail if Certificate Services is not running. If Certificate Services is running and ready to accept requests, this function will return S_OK, and *<i>pfServerOnline</i> will point to a value of <b>TRUE</b>. If Certificate Services is running in suspended (or paused) mode, this function will return S_OK, and *<i>pfServerOnline</i> will point to a value of <b>FALSE</b>.

## -remarks

Call this function to determine whether a Certificate Services server is online and available for backup operations.

This function's name in Certadm.dll is <b>CertSrvIsServerOnlineW</b>. You must use this form of the name when calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVISSERVERONLINEW</b> in the Certbcli.h header file.


#### Examples


```cpp
FNCERTSRVISSERVERONLINEW* pfnOnline = NULL;
char * szOnlineFunc = "CertSrvIsServerOnlineW";
BOOL       bOnline = 0;
HRESULT    hr = 0;

// Get the address of the function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnOnline = (FNCERTSRVISSERVERONLINEW*) GetProcAddress(hInst,
                                        szOnlineFunc );
if ( NULL == pfnOnline )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szOnlineFunc,
           GetLastError() );
    exit(1);  // Or other appropriate error action.
}

// Call the function; wszServer was set earlier to the server name.
hr = pfnOnline(wszServer, &bOnline);
if (FAILED(hr))
{
    printf("Failed pfnOnline, hr=%x, err=%d\n",
           hr,
           GetLastError());
    exit(1);  // Or other appropriate error action.
}

// Display the online status.
printf("Server is %s\n", 
       (bOnline ? "Online" : "Suspended" ));
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackuppreparew">CertSrvBackupPrepare</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>