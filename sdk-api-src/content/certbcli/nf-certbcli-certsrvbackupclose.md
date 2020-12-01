---
UID: NF:certbcli.CertSrvBackupClose
title: CertSrvBackupClose function (certbcli.h)
description: Closes the file opened by the CertSrvBackupOpenFile function.
helpviewer_keywords: ["CertSrvBackupClose","CertSrvBackupClose function [Security]","_certsrv_certsrvbackupclose","certbcli/CertSrvBackupClose","security.certsrvbackupclose"]
old-location: security\certsrvbackupclose.htm
tech.root: security
ms.assetid: 123933b4-5496-460d-aaaa-a494786cd638
ms.date: 12/05/2018
ms.keywords: CertSrvBackupClose, CertSrvBackupClose function [Security], _certsrv_certsrvbackupclose, certbcli/CertSrvBackupClose, security.certsrvbackupclose
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
 - CertSrvBackupClose
 - certbcli/CertSrvBackupClose
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
 - CertSrvBackupClose
---

# CertSrvBackupClose function


## -description

The <b>CertSrvBackupClose</b>  function closes the file opened by the 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a> function.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup context.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

For every successful call to <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a>, there should be a subsequent call to <b>CertSrvBackupClose</b>. Upon completion of backing up a  file, the file needs to be closed.


#### Examples


```cpp
FNCERTSRVBACKUPCLOSE* pfnClose;
char * szBackupCloseFunc = "CertSrvBackupClose";
HRESULT    hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnClose = (FNCERTSRVBACKUPCLOSE*)GetProcAddress(hInst,
                                   szBackupCloseFunc);
if ( NULL == pfnClose )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
            szBackupCloseFunc,
            GetLastError() );
    exit(1);  // Or other appropriate error action.
}
// Close the file.
// hCSBC represents an HCSBC used in
// an earlier call to CertSrvBackupOpenFile.
hr = pfnClose(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnClose call [%x]\n", hr);
    exit(1);  // Or other appropriate error action.
}
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupopenfilew">CertSrvBackupOpenFile</a>



<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackupread">CertSrvBackupRead</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>