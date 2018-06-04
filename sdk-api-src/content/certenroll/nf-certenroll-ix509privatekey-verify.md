---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IX509PrivateKey::Verify


## -description


The <b>Verify</b> method verifies that a private key exists and can be used by the client but does not open the key.


## -parameters




### -param VerifyType [in]

An <a href="https://msdn.microsoft.com/23466035-6554-490f-ad46-e97ba5a5d996">X509PrivateKeyVerify</a> enumeration value that specifies execution options for the method. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VerifyNone"></a><a id="verifynone"></a><a id="VERIFYNONE"></a><dl>
<dt><b><b>VerifyNone</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySilent"></a><a id="verifysilent"></a><a id="VERIFYSILENT"></a><dl>
<dt><b><b>VerifySilent</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if a user interface is required to open the private key; otherwise verification occurs. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySmartCardNone"></a><a id="verifysmartcardnone"></a><a id="VERIFYSMARTCARDNONE"></a><dl>
<dt><b><b>VerifySmartCardNone</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if the key is stored on a smart card; otherwise, this value is equivalent to  <b>VerifyAllowUI</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySmartCardSilent"></a><a id="verifysmartcardsilent"></a><a id="VERIFYSMARTCARDSILENT"></a><dl>
<dt><b><b>VerifySmartCardSilent</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if a user interface is required to open the private key and the key is stored on a smart card;  otherwise, this value is equivalent to   <b>VerifyAllowUI</b>. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifyAllowUI"></a><a id="verifyallowui"></a><a id="VERIFYALLOWUI"></a><dl>
<dt><b><b>VerifyAllowUI</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The method allows a user interface to be displayed.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. Also, this method calls the <a href="https://msdn.microsoft.com/d9166b98-e5f1-4e5c-b6f1-2a086b102e0f">CryptGetUserKey</a> and <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>
CryptoAPI functions and can return errors identified in that documentation. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
Properties related to the CSP or KSP could not be found.

</td>
</tr>
</table>
 




## -remarks



If <b>VerifySilent</b> or <b>VerifySmartCardSilent</b> values are set and the cryptographic provider specifies that a user interface is necessary, the key will not be opened, but the method returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

