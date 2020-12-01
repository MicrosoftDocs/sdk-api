---
UID: NF:certbcli.CertSrvBackupEnd
title: CertSrvBackupEnd function (certbcli.h)
description: Ends a Certificate Services backup session.
helpviewer_keywords: ["CertSrvBackupEnd","CertSrvBackupEnd function [Security]","_certsrv_certsrvbackupend","certbcli/CertSrvBackupEnd","security.certsrvbackupend"]
old-location: security\certsrvbackupend.htm
tech.root: security
ms.assetid: ebf87af3-df45-4440-9881-e2926b0c4f08
ms.date: 12/05/2018
ms.keywords: CertSrvBackupEnd, CertSrvBackupEnd function [Security], _certsrv_certsrvbackupend, certbcli/CertSrvBackupEnd, security.certsrvbackupend
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
 - CertSrvBackupEnd
 - certbcli/CertSrvBackupEnd
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
 - CertSrvBackupEnd
---

# CertSrvBackupEnd function


## -description

The <b>CertSrvBackupEnd</b> function ends a Certificate Services backup session.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup context.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

Upon completion of a backup session, the session needs to be terminated by means of <b>CertSrvBackupEnd</b>. For every successful call to <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackuppreparew">CertSrvBackupPrepare</a>, there should be a call to <b>CertSrvBackupEnd</b>.


#### Examples


```cpp
FNCERTSRVBACKUPEND* pfnBackupEnd;
char * szBackEndFunc = "CertSrvBackupEnd";
HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnBackupEnd = (FNCERTSRVBACKUPEND*)GetProcAddress(hInst,
                                       szBackEndFunc);
if (NULL == pfnBackupEnd)
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackEndFunc,
           GetLastError() );
    exit(1);  // Or other appropriate error action.
}

// When done, release the HCSBC.
// hCSBC would have been created by an earlier call
// to CertSrvBackupPrepare.
hr = pfnBackupEnd(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnBackupEnd call [%x]\n", hr);
    exit(1);  // Or other appropriate error action.
}
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvbackuppreparew">CertSrvBackupPrepare</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>