---
UID: NF:wincrypt.CertEnumCTLsInStore
title: CertEnumCTLsInStore function
author: windows-sdk-content
description: The CertEnumCTLsInStore function retrieves the first or next certificate trust list (CTL) context in a certificate store. Used in a loop, this function can retrieve in sequence all CTL contexts in a certificate store.
old-location: security\certenumctlsinstore.htm
tech.root: seccrypto
ms.assetid: dac9f91e-8ed4-43ce-8147-485c2ed7edd5
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CertEnumCTLsInStore, CertEnumCTLsInStore function [Security], _crypto2_certenumctlsinstore, security.certenumctlsinstore, wincrypt/CertEnumCTLsInStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertEnumCTLsInStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertEnumCTLsInStore function


## -description


The <b>CertEnumCTLsInStore</b> function retrieves the first or next <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. Used in a loop, this function can retrieve in sequence all CTL contexts in a certificate store.


## -parameters




### -param hCertStore [in]

Handle of a certificate store.


### -param pPrevCtlContext [in]

A pointer to the previous 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure found. It must be <b>NULL</b> to get the first CTL in the store. Successive CTLs are enumerated by setting <i>pPrevCtlContext</i> to the pointer returned by a previous call. This function frees the <b>CTL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter. The enumeration skips any CTLs previously deleted by 
<a href="https://msdn.microsoft.com/e24d3445-8929-463a-b771-1f25f4e999b5">CertDeleteCTLFromStore</a>.


## -returns



If the function succeeds, the return value is a pointer to a read-only 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>.

If the function fails and a CTL is not found, the return value is <b>NULL</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Either no CTLs exist in the store, or the function reached the end of the store's list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CTL context pointed to by the <i>pPrevCtlContext</i> parameter.

</td>
</tr>
</table>
 




## -remarks



The returned pointer is freed when passed as the <i>pPrevCtlContext</i> on a subsequent call. Otherwise, the pointer must be explicitly freed by calling 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>. A <i>pPrevCtlContext</i> that is not <b>NULL</b> is always freed by this function (through a call to <b>CertFreeCTLContext</b>), even for an error.

A duplicate can be made by calling 
<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/e24d3445-8929-463a-b771-1f25f4e999b5">CertDeleteCTLFromStore</a>



<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>



<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Trust List Functions</a>
 

 

