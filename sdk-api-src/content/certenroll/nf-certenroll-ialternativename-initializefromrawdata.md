---
UID: NF:certenroll.IAlternativeName.InitializeFromRawData
title: IAlternativeName::InitializeFromRawData
author: windows-sdk-content
description: Initializes the object from a Digital Signature Algorithm (DSA) GUID, an X.500 directory name, or an Internet Protocol (IP) address contained in a Distinguished Encoding Rules (DER) encoded byte array.
old-location: security\ialternativename_initializefromrawdata_method.htm
tech.root: SecCertEnroll
ms.assetid: 1559801c-ec62-471e-851f-f67219565cd1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromRawData method, IAlternativeName.InitializeFromRawData, IAlternativeName::InitializeFromRawData, InitializeFromRawData, InitializeFromRawData method [Security], InitializeFromRawData method [Security],IAlternativeName interface, XCN_CERT_ALT_NAME_DIRECTORY_NAME, XCN_CERT_ALT_NAME_GUID, XCN_CERT_ALT_NAME_IP_ADDRESS, certenroll/IAlternativeName::InitializeFromRawData, security.ialternativename_initializefromrawdata_method
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
 - IAlternativeName.InitializeFromRawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlternativeName::InitializeFromRawData


## -description


The <b>InitializeFromRawData</b> method initializes the object from a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) GUID, an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> directory name, or an Internet Protocol (IP) address contained in a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array.


## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/79b675cc-c979-46ab-aee1-0031af2efd40">AlternativeNameType</a> enumeration value that identifies the type of name represented by the input string. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_DIRECTORY_NAME"></a><a id="xcn_cert_alt_name_directory_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_DIRECTORY_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an X.500 directory name.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_IP_ADDRESS"></a><a id="xcn_cert_alt_name_ip_address"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_IP_ADDRESS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_GUID"></a><a id="xcn_cert_alt_name_guid"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_GUID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a GUID.

</td>
</tr>
</table>
 


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that identifies the type of Unicode encoding applied to the <i>strRawData</i> parameter.


### -param strRawData [in]

A <b>BSTR</b> variable that contains the DER-encoded data.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



The raw data is a byte array that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER). You must specify the  byte array as a Unicode encoded string.

If you use this method to specify a DSA GUID (XCN_CERT_ALT_NAME_GUID), the GUID is associated with the XCN_OID_NTDS_REPLICATION (1.3.6.1.4.1.311.25.1) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and encoded as an octet string (byte array). You can retrieve the OID by calling the <a href="https://msdn.microsoft.com/be14756b-a7dc-40f4-ae09-b576f85837f6">ObjectId</a> property. You can call the <a href="https://msdn.microsoft.com/7385654d-03f8-4796-a95c-000fa8ab65a3">RawData</a> property to retrieve the encoded byte array.

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
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a DNS name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered OID.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN).</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an OID and a byte array.</td>
</tr>
</table>
 



You can use the <a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a> method to specify an OID and a corresponding name string, and you can use the <a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a> method to specify an email address, a DNS name, a URL, a registered OID, or a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN).




## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>
 

 

