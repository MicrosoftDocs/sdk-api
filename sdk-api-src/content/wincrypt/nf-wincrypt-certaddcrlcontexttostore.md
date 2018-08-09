---
UID: NF:wincrypt.CertAddCRLContextToStore
title: CertAddCRLContextToStore function
author: windows-sdk-content
description: Adds a certificate revocation list (CRL) context to the specified certificate store.
old-location: security\certaddcrlcontexttostore.htm
old-project: seccrypto
ms.assetid: 5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCRLContextToStore, CertAddCRLContextToStore function [Security], _crypto2_certaddcrlcontexttostore, security.certaddcrlcontexttostore, wincrypt/CertAddCRLContextToStore
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertAddCRLContextToStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertAddCRLContextToStore function


## -description


The <b>CertAddCRLContextToStore</b> function adds a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context to the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


## -parameters




### -param hCertStore [in]

Handle of a certificate store.


### -param pCrlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure to be added.


### -param dwAddDisposition [in]

Specifies the action to take if a matching CRL or a link to a matching CRL already exists in the store. Currently defined disposition values and their uses are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_ALWAYS"></a><a id="cert_store_add_always"></a><dl>
<dt><b>CERT_STORE_ADD_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Makes no check for an existing matching CRL or link to a matching CRL. A new CRL is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, the operation fails. 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER"></a><a id="cert_store_add_newer"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, the function compares the <b>ThisUpdate</b> times on the CRLs. If the existing CRL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CRL, the old CRL or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CRL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CRL to be added, the function fails with 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returning the CRYPT_E_EXISTS code.

If a matching CRL or a link to a matching CRL is not found in the store, a new CRL is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The action is the same as for CERT_STORE_ADD_NEWER, except that if an older CRL is replaced, the properties of the older CRL are incorporated into the replacement CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, the existing CRL or link is deleted and a new CRL is created and added to the store. If a matching CRL or a link to a matching CRL does not exist, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL exists in the store, the existing context is deleted before creating and adding the new context. The added context inherits properties from the existing CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, that existing CRL is used and properties from the new CRL are added. The function does not fail, but no new CRL is added. If <i>ppCertContext</i> is not <b>NULL</b>, the existing context is duplicated. 




If a matching CRL or a link to a matching CRL does not exist, a new CRL is added.

</td>
</tr>
</table>
 


### -param ppStoreContext [out, optional]

A pointer to a pointer to the decoded CRL context. This is an optional parameter and can be <b>NULL</b>, indicating that the calling application does not require a copy of the added or existing CRL. If a copy is made, that context must be freed by using 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Errors from the called functions 
<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a> and 
<a href="https://msdn.microsoft.com/7e4a0a39-ce55-4171-9b66-31c1c28d895f">CertSetCRLContextProperty</a> can be propagated to this function.

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
This error is returned if CERT_STORE_ADD_NEW is set and the CRL already exists in the store or if CERT_STORE_ADD_NEWER is set and a CRL exists in the store with a <b>ThisUpdate</b> date greater than or equal to the <b>ThisUpdate</b> date on the CRL to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwAddDisposition</i> parameter specified a disposition value that is not valid.

</td>
</tr>
</table>
 




## -remarks



The CRL context is not duplicated using 
<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>. Instead, a new copy is created and added to the store. In addition to copying the encoded CRL, the function copies the context's properties.

To remove the CRL context from the certificate store, use the  <a href="https://msdn.microsoft.com/eb542c25-8d2b-4427-8f2a-719b472613a5">CertDeleteCRLFromStore</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a>



<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="https://msdn.microsoft.com/7e4a0a39-ce55-4171-9b66-31c1c28d895f">CertSetCRLContextProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Revocation List Functions</a>
 

 

