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

# ICertEncodeStringArray::GetStringType


## -description


The <b>GetStringType</b> method returns the type of string values that the string array contains.


## -parameters




### -param pStringType [out]

A pointer to a <b>Long</b> that  represents the string type. For a list of string types, see Remarks.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value indicates the type of strings in the string array. For a list of string types, see Remarks.




## -remarks



The following table lists the types of strings that the string array can  contain. For more information about RDN types, see the CryptoAPI 2.0 documents.

<table>
<tr>
<th>String type</th>
<th>Meaning</th>
</tr>
<tr>
<td>CERT_RDN_ANY_TYPE</td>
<td>For encoding an X509_UNICODE_NAME name.</td>
</tr>
<tr>
<td>CERT_RDN_NUMERIC_STRING</td>
<td>The numerals 0 through 9 and the space character (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_PRINTABLE_STRING</td>
<td>Printable characters (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_T61_STRING</td>
<td>T.61 encoded characters (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_VIDEOTEX_STRING</td>
<td>VIDEOTEX characters.</td>
</tr>
<tr>
<td>CERT_RDN_IA5_STRING</td>
<td>IA5 (ASCII) characters.</td>
</tr>
<tr>
<td>CERT_RDN_GRAPHIC_STRING</td>
<td>A string of ISO-defined GRAPHIC characters.</td>
</tr>
<tr>
<td>CERT_RDN_ISO646_STRING</td>
<td>128 character set (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_GENERAL_STRING</td>
<td>A string of ISO-defined GENERAL characters.</td>
</tr>
<tr>
<td>CERT_RDN_INT4_STRING</td>
<td>An array of INT4 values (32 bit).</td>
</tr>
<tr>
<td>CERT_RDN_UNICODE_STRING</td>
<td><a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> characters (16 bit).</td>
</tr>
</table>
 


#### Examples

For an example that uses the <b>GetStringType</b> method, see the <a href="https://msdn.microsoft.com/d8fc51ea-4d83-402a-a4ac-ce55d385905c">ICertEncodeStringArray::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5515c25e-f788-4222-8f66-f5d86bd2a3a3">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/125524ae-236d-4507-9c00-76a016bf6c62">ICertEncodeStringArray::Reset</a>
 

 

