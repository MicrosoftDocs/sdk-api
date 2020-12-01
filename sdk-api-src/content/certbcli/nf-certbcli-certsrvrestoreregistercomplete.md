---
UID: NF:certbcli.CertSrvRestoreRegisterComplete
title: CertSrvRestoreRegisterComplete function (certbcli.h)
description: Completes a registered Certificate Services restore operation.
helpviewer_keywords: ["CertSrvRestoreRegisterComplete","CertSrvRestoreRegisterComplete function [Security]","_certsrv_certsrvrestoreregistercomplete","certbcli/CertSrvRestoreRegisterComplete","security.certsrvrestoreregistercomplete"]
old-location: security\certsrvrestoreregistercomplete.htm
tech.root: security
ms.assetid: 1459d5b2-2c12-48df-ae01-c713c86f1c2e
ms.date: 12/05/2018
ms.keywords: CertSrvRestoreRegisterComplete, CertSrvRestoreRegisterComplete function [Security], _certsrv_certsrvrestoreregistercomplete, certbcli/CertSrvRestoreRegisterComplete, security.certsrvrestoreregistercomplete
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
 - CertSrvRestoreRegisterComplete
 - certbcli/CertSrvRestoreRegisterComplete
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
 - CertSrvRestoreRegisterComplete
---

# CertSrvRestoreRegisterComplete function


## -description

The <b>CertSrvRestoreRegisterComplete</b>  function completes a registered Certificate Services restore operation.

## -parameters

### -param hbc [in]

A handle to a Certificate Services restore context. You must set this handle by calling 
<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterw">CertSrvRestoreRegister</a> before using it in <b>CertSrvRestoreRegisterComplete</b>.

### -param hrRestoreState [in]

<b>HRESULT</b> value indicating the success code for the restore operation. Set this value to S_OK if the restore operation was successful.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

If a registered restore operation is not completed, Certificate Services will not start.


#### Examples


```cpp
FNCERTSRVRESTOREREGISTERCOMPLETE* pfnRestRegComplete;
char * szResRegCompleteFunc = "CertSrvRestoreRegisterComplete";
HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnRestRegComplete = (FNCERTSRVRESTOREREGISTERCOMPLETE*)
                     GetProcAddress( hInst, szResRegCompleteFunc );
if ( NULL == pfnRestRegComplete )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szResRegCompleteFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Complete a registered restoration operation.
// hCSBC is an HCSBC variable used in a previous
// call to CertSrvRestoreRegister.
hr = pfnRestRegComplete(hCSBC, S_OK);
if (FAILED(hr))
{
    printf("Failed pfnRestRegComplete call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreregisterw">CertSrvRestoreRegister</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>