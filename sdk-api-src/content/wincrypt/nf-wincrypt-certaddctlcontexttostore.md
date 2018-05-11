---
UID: NF:wincrypt.CertAddCTLContextToStore
title: CertAddCTLContextToStore function
author: windows-driver-content
description: Adds a certificate trust list (CTL) context to a certificate store.
old-location: security\certaddctlcontexttostore.htm
old-project: SecCrypto
ms.assetid: e8858f75-77a1-4c5f-a3e3-a645c5e0f053
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCTLContextToStore, CertAddCTLContextToStore function [Security], _crypto2_certaddctlcontexttostore, security.certaddctlcontexttostore, wincrypt/CertAddCTLContextToStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertAddCTLContextToStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertAddCTLContextToStore function


## -description



			The <b>CertAddCTLContextToStore</b> function adds a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


## -parameters




### -param hCertStore [in]

Handle of a certificate store.


### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure to be added to the store.


### -param dwAddDisposition [in]

Specifies the action to take if a matching CTL or a link to a matching CTL already exists in the store. Currently defined disposition values and their uses are as follows.

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
Makes no check for an existing matching CTL or link to a matching CTL. A new CTL is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the operation fails. 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER"></a><a id="cert_store_add_newer"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the <b>ThisUpdate</b> times on the CTLs are compared. If the existing CTL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CTL, the old CTL or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CTL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CTL to be added, the function fails with 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returning the CRYPT_E_EXISTS code.

If a matching CTL or a link to a matching CTL is not found in the store, a new CTL is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The action is the same as for CERT_STORE_ADD_NEWER, except that if an older CTL is replaced, the properties of the older CTL are incorporated into the replacement CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the existing CTL or link is deleted and a new CTL is created and added to the store. If a matching CTL or a link to a matching CTL does not exist, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL exists in the store, that existing context is deleted before creating and adding the new context. The added context inherits properties from the existing CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, that existing CTL is used and properties from the new CTL are added. The function does not fail, but no new CTL is added. If <i>ppCertContext</i> is not <b>NULL</b>, the existing context is duplicated.

If a matching CTL or a link to a matching CTL does not exist, a new CTL is added.

</td>
</tr>
</table>
 


### -param ppStoreContext [out, optional]

Pointer to a pointer to the decoded CTL <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>. This optional parameter can be <b>NULL</b> indicating that the calling application does not require a copy of the added or existing CTL. If a copy is made, that context must be freed using 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>.


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
This error is returned if CERT_STORE_ADD_NEW is set and the CTL exists in the store or if CERT_STORE_ADD_NEWER is set and a CTL exists in the store with a <b>ThisUpdate</b> date greater than or equal to the <b>ThisUpdate</b> date on the CTL to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An add disposition that is not valid was specified by the <i>dwAddDisposition</i> parameter.

</td>
</tr>
</table>
 




## -remarks



The CTL context is not duplicated using 
<a href="https://msdn.microsoft.com/512d246f-9f22-4ac1-a4fc-d5c615a65cf9">CertDuplicateCTLContext</a>. Instead, a new copy is created and added to the store. In addition to the encoded CTL, the context's properties are copied.

To remove the CTL context from the certificate store, use the  <a href="https://msdn.microsoft.com/e24d3445-8929-463a-b771-1f25f4e999b5">CertDeleteCTLFromStore</a> function.




## -see-also




<a href="https://msdn.microsoft.com/4239d43e-187d-4f40-99ae-6f914b7577ac">CertAddEncodedCTLToStore</a>



<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a>



<a href="cryptography_functions.htm">Certificate Trust List Functions</a>
 

 

