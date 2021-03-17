---
UID: NF:certbcli.CertSrvRestoreEnd
title: CertSrvRestoreEnd function (certbcli.h)
description: Ends a Certificate Services restore session.
helpviewer_keywords: ["CertSrvRestoreEnd","CertSrvRestoreEnd function [Security]","_certsrv_certsrvrestoreend","certbcli/CertSrvRestoreEnd","security.certsrvrestoreend"]
old-location: security\certsrvrestoreend.htm
tech.root: security
ms.assetid: 59316edc-a677-47ff-a139-565d7b5507fb
ms.date: 12/05/2018
ms.keywords: CertSrvRestoreEnd, CertSrvRestoreEnd function [Security], _certsrv_certsrvrestoreend, certbcli/CertSrvRestoreEnd, security.certsrvrestoreend
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
 - CertSrvRestoreEnd
 - certbcli/CertSrvRestoreEnd
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
 - CertSrvRestoreEnd
---

# CertSrvRestoreEnd function


## -description

The <b>CertSrvRestoreEnd</b> function ends a Certificate Services restore session.

## -parameters

### -param hbc [in]

A handle to a Certificate Services backup context.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -remarks

When a restore session is complete, terminate the session by calling <b>CertSrvRestoreEnd</b>. For every successful call to <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestorepreparew">CertSrvRestorePrepare</a>, there should be a call to <b>CertSrvRestoreEnd</b>.

When a restore is complete, it is important that you make a new full backup of the Certificate Services database. This is necessary to truncate the restored log files and to establish a base backup set for future restores. Backups performed after a restore cannot be mixed with backups (full or incremental) taken before the restore; that is, after a certificate services database is restored and has progressed to a subsequent state, you cannot use the pre-restoration backups to restore the database to that subsequent state.


#### Examples


```cpp
FNCERTSRVRESTOREEND*  pfnRestoreEnd;
char * szRestoreEndFunc = "CertSrvRestoreEnd";
HRESULT    hr=0;
	
// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnRestoreEnd = (FNCERTSRVRESTOREEND*)GetProcAddress(hInst,
                                  szRestoreEndFunc);
if ( NULL == pfnRestoreEnd )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szRestoreEndFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// When done, release the HCSBC.
// hCSBC would have been set by an earlier call
// to CertSrvRestorePrepare.
hr = pfnRestoreEnd(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnRestoreEnd call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestorepreparew">CertSrvRestorePrepare</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>