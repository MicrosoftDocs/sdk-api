---
UID: NF:certenroll.IAlternativeName.InitializeFromString
title: IAlternativeName::InitializeFromString
author: windows-sdk-content
description: Initializes the object from a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered object identifier (OID), or a user principal name (UPN).
old-location: security\ialternativename_initializefromstring_method.htm
tech.root: seccertenroll
ms.assetid: 7b5f7dd3-00dc-474b-8920-45a3acded209
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromString method, IAlternativeName.InitializeFromString, IAlternativeName::InitializeFromString, InitializeFromString, InitializeFromString method [Security], InitializeFromString method [Security],IAlternativeName interface, XCN_CERT_ALT_NAME_DNS_NAME, XCN_CERT_ALT_NAME_REGISTERED_ID, XCN_CERT_ALT_NAME_RFC822_NAME, XCN_CERT_ALT_NAME_URL, XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, certenroll/IAlternativeName::InitializeFromString, security.ialternativename_initializefromstring_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IAlternativeName.InitializeFromString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlternativeName::InitializeFromString


## -description


The <b>InitializeFromString</b> method initializes the object from a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID), or a <a href="https://msdn.microsoft.com/en-us/library/ms721629(v=VS.85).aspx">user principal name</a> (UPN).


## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374830(v=VS.85).aspx">AlternativeNameType</a> enumeration value that identifies the type of name represented by the input string contained in the <i>strValue</i> parameter. This must be one of the following values.

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



If you use this method to specify a UPN, the UPN is associated with the XCN_OID_NT_PRINCIPAL_NAME (1.3.6.1.4.1.311.20.2.3) OID and is <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded. You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa375037(v=VS.85).aspx">RawData</a> property to retrieve the encoded byte array. You can retrieve the OID by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375030(v=VS.85).aspx">ObjectId</a> property.

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
<td>The name is an <a href="https://msdn.microsoft.com/en-us/library/ms721636(v=VS.85).aspx">X.500</a> directory name.</td>
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
 



You can use the <a href="https://msdn.microsoft.com/en-us/library/Aa375017(v=VS.85).aspx">InitializeFromOtherName</a> method to specify an OID and a corresponding name string, and you can use the <a href="https://msdn.microsoft.com/en-us/library/Aa375021(v=VS.85).aspx">InitializeFromRawData</a> method to specify a GUID, IP address, or X.500 directory name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374984(v=VS.85).aspx">IAlternativeNames</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a>
 

 

