---
UID: NF:certbcli.CertSrvRestorePrepareW
title: CertSrvRestorePrepareW function (certbcli.h)
description: Prepares a Certificate Services instance for restore operations.
helpviewer_keywords: ["CSRESTORE_TYPE_FULL","CertSrvRestorePrepare","CertSrvRestorePrepare function [Security]","CertSrvRestorePrepareW","_certsrv_certsrvrestoreprepare","certbcli/CertSrvRestorePrepare","certbcli/CertSrvRestorePrepareW","security.certsrvrestoreprepare"]
old-location: security\certsrvrestoreprepare.htm
tech.root: security
ms.assetid: e607b61c-9636-40e6-abba-74152f37b49e
ms.date: 12/05/2018
ms.keywords: CSRESTORE_TYPE_FULL, CertSrvRestorePrepare, CertSrvRestorePrepare function [Security], CertSrvRestorePrepareW, _certsrv_certsrvrestoreprepare, certbcli/CertSrvRestorePrepare, certbcli/CertSrvRestorePrepareW, security.certsrvrestoreprepare
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvRestorePrepareW (Unicode)
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
 - CertSrvRestorePrepareW
 - certbcli/CertSrvRestorePrepareW
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
 - CertSrvRestorePrepare
 - CertSrvRestorePrepareW
---

# CertSrvRestorePrepareW function


## -description

The <b>CertSrvRestorePrepare</b>  function  prepares a Certificate Services instance for restore operations.

## -parameters

### -param pwszServerName [in]

A pointer to the computer name of the server to prepare for restore operations. This name can be the NetBIOS name or the DNS name.

### -param dwRestoreFlags [in]

A bitfield that represents the combination of values in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSRESTORE_TYPE_FULL"></a><a id="csrestore_type_full"></a><dl>
<dt><b>CSRESTORE_TYPE_FULL</b></dt>
</dl>
</td>
<td width="60%">
Restore Certificate Services database, logs, and related files.

</td>
</tr>
</table>

### -param phbc [out]

A pointer to a Certificate Services backup context handle (<b>HCSBC</b>).

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success, and *<i>phbc</i> is set to an <b>HCSBC</b>, which can be used by other Certificate Services restore APIs.

## -remarks

Before a Certificate Services restore operation can occur, it is necessary to create an <b>HCSBC</b> by means of <b>CertSrvRestorePrepare</b>. This <b>HCSBC</b> can be used by various Certificate Services restore functions.

<div class="alert"><b>Note</b>  When the restore session is completed, it is necessary to call <a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreend">CertSrvRestoreEnd</a> to release the <b>HCSBC</b> which resulted from the call to <b>CertSrvRestorePrepare</b>.</div>
<div> </div>
This function's name in Certadm.dll is <b>CertSrvRestorePrepareW</b>. You must use this form of the name when calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVRESTOREPREPAREW</b> in the Certbcli.h header file.

To execute this call, you must have the restore <a href="/windows/desktop/SecGloss/p-gly">privilege</a>. For more information, see 
<a href="/windows/desktop/SecCrypto/setting-the-backup-and-restore-privileges">Setting the Backup and Restore Privileges</a>.


#### Examples


```cpp
FNCERTSRVRESTOREPREPAREW*  pfnRestorePrepare;
char * szRestorePrepFunc = "CertSrvRestorePrepareW";
HCSBC      hCSBC=NULL;
HINSTANCE  hInst=0;
HRESULT    hr=0;

// Load the DLL.
hInst = LoadLibrary(L"Certadm.dll");
if ( NULL == hInst )
{
    printf("Failed LoadLibrary,error=%d\n",
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Get the address for the desired function.
pfnRestorePrepare = (FNCERTSRVRESTOREPREPAREW*)GetProcAddress( hInst,
                                          szRestorePrepFunc );
if ( NULL == pfnRestorePrepare )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szRestorePrepFunc,
           GetLastError() );
    exit(1); // Or other appropriate error action.
}

// Prepare CertServ for restoration.
hr = pfnRestorePrepare(wszServer,
                       CSRESTORE_TYPE_FULL,
                       &hCSBC);

if (FAILED(hr))
{
    printf("Failed pfnRestorePrepare call [%x]\n", hr);
    exit(1); // Or other appropriate error action.
}

// Use the HCSBC for restore operations.
// ...


// When done processing, release the HCSBC context
// by calling CertSrvRestoreEnd (not shown here).
// ...

// Free the DLL.
if (hInst)
    FreeLibrary(hInst);
```

## -see-also

<a href="/windows/desktop/api/certbcli/nf-certbcli-certsrvrestoreend">CertSrvRestoreEnd</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/SecCrypto/setting-the-backup-and-restore-privileges">Setting the Backup and Restore Privileges</a>



<a href="/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions">Using the Certificate Services Backup and Restore Functions</a>