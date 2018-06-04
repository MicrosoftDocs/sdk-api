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

# IAlternativeName::InitializeFromString


## -description


The <b>InitializeFromString</b> method initializes the object from a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), or a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN).


## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/79b675cc-c979-46ab-aee1-0031af2efd40">AlternativeNameType</a> enumeration value that identifies the type of name represented by the input string contained in the <i>strValue</i> parameter. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_RFC822_NAME"></a><a id="xcn_cert_alt_name_rfc822_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_RFC822_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an email address.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_DNS_NAME"></a><a id="xcn_cert_alt_name_dns_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_DNS_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a DNS name.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_URL"></a><a id="xcn_cert_alt_name_url"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_URL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a URL.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_REGISTERED_ID"></a><a id="xcn_cert_alt_name_registered_id"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_REGISTERED_ID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a registered OID.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME"></a><a id="xcn_cert_alt_name_user_principle_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a UPN.

</td>
</tr>
</table>
 


### -param strValue [in]

A <b>BSTR</b> variable that contains the name.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If you use this method to specify a UPN, the UPN is associated with the XCN_OID_NT_PRINCIPAL_NAME (1.3.6.1.4.1.311.20.2.3) OID and is <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded. You can call the <a href="https://msdn.microsoft.com/7385654d-03f8-4796-a95c-000fa8ab65a3">RawData</a> property to retrieve the encoded byte array. You can retrieve the OID by calling the <a href="https://msdn.microsoft.com/be14756b-a7dc-40f4-ae09-b576f85837f6">ObjectId</a> property.

If you use this method to specify any of the following name types, the method returns <b>E_INVALIDARG</b>.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_UNKNOWN</td>
<td>The name type is not identified.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an OID and a byte array.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> directory name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an IP address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID.</td>
</tr>
</table>
 



You can use the <a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a> method to specify an OID and a corresponding name string, and you can use the <a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a> method to specify a GUID, IP address, or X.500 directory name.




## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>



<a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a>



<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 

