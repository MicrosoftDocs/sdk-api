---
UID: NF:wincrypt.CertEnumCRLsInStore
title: CertEnumCRLsInStore function
author: windows-sdk-content
description: The CertEnumCRLsInStore function retrieves the first or next certificate revocation list (CRL) context in a certificate store. Used in a loop, this function can retrieve in sequence all CRL contexts in a certificate store.
old-location: security\certenumcrlsinstore.htm
tech.root: seccrypto
ms.assetid: fc25ca04-8520-4053-9591-afc81c88670c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CertEnumCRLsInStore, CertEnumCRLsInStore function [Security], _crypto2_certenumcrlsinstore, security.certenumcrlsinstore, wincrypt/CertEnumCRLsInStore
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
 - CertEnumCRLsInStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertEnumCRLsInStore function


## -description


The <b>CertEnumCRLsInStore</b> function retrieves the first or next <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>. Used in a loop, this function can retrieve in sequence all CRL contexts in a certificate store.


## -parameters




### -param hCertStore [in]

Handle of a certificate store.


### -param pPrevCrlContext [in]

A pointer to the previous 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure found. The <i>pPrevCrlContext</i> parameter must be <b>NULL</b> to get the first CRL in the store. Successive CRLs are enumerated by setting <i>pPrevCrlContext</i> to the pointer returned by a previous call to the function.  This function frees the <b>CRL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter. The enumeration skips any CRLs previously deleted by 
<a href="https://msdn.microsoft.com/eb542c25-8d2b-4427-8f2a-719b472613a5">CertDeleteCRLFromStore</a>.


## -returns



If the function succeeds, the return value is a pointer to the next 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> in the store.

<b>NULL</b> is returned if the function fails. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the certificate context pointed to by <i>pPrevCrlContext</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No CRL was found. This happens if the store is empty or the end of the store's list is reached.

</td>
</tr>
</table>
 




## -remarks



The returned pointer is freed when it is passed as the <i>pPrevCrlContext</i> on a subsequent call to the function. Otherwise, the pointer must explicitly be freed by calling 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>. A <i>pPrevCrlContext</i> that is not <b>NULL</b> is always freed when passed to this function through a call to <b>CertFreeCRLContext</b>, even if the function itself returns an error.

A duplicate of the CRL <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> returned by this function can be made by calling 
<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>



<a href="https://msdn.microsoft.com/eb542c25-8d2b-4427-8f2a-719b472613a5">CertDeleteCRLFromStore</a>



<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>



<a href="https://msdn.microsoft.com/3e481912-204a-4d86-ab67-81f8ae4d1aaa">CertFindCRLInStore</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="cryptography_functions.htm">Certificate Revocation List Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

