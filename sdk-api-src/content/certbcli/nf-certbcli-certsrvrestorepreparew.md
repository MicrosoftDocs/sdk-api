---
UID: NF:certbcli.CertSrvRestorePrepareW
title: CertSrvRestorePrepareW function
author: windows-sdk-content
description: Prepares a Certificate Services instance for restore operations.
old-location: security\certsrvrestoreprepare.htm
tech.root: seccrypto
ms.assetid: e607b61c-9636-40e6-abba-74152f37b49e
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CSRESTORE_TYPE_FULL, CertSrvRestorePrepare, CertSrvRestorePrepare function [Security], CertSrvRestorePrepareW, _certsrv_certsrvrestoreprepare, certbcli/CertSrvRestorePrepare, certbcli/CertSrvRestorePrepareW, security.certsrvrestoreprepare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

<div class="alert"><b>Note</b>  When the restore session is completed, it is necessary to call <a href="https://msdn.microsoft.com/en-us/library/Aa376998(v=VS.85).aspx">CertSrvRestoreEnd</a> to release the <b>HCSBC</b> which resulted from the call to <b>CertSrvRestorePrepare</b>.</div>
<div> </div>
This function's name in Certadm.dll is <b>CertSrvRestorePrepareW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVRESTOREPREPAREW</b> in the Certbcli.h header file.

To execute this call, you must have the restore <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">privilege</a>. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa387705(v=VS.85).aspx">Setting the Backup and Restore Privileges</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa376998(v=VS.85).aspx">CertSrvRestoreEnd</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa387705(v=VS.85).aspx">Setting the Backup and Restore Privileges</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa388174(v=VS.85).aspx">Using the Certificate Services Backup and Restore Functions</a>
 

 

