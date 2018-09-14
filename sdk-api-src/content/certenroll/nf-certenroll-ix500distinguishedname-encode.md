---
UID: NF:certenroll.IX500DistinguishedName.Encode
title: IX500DistinguishedName::Encode
author: windows-sdk-content
description: Initializes the object from a string that contains a distinguished name.
old-location: security\ix500distinguishedname_encode_method.htm
tech.root: seccertenroll
ms.assetid: da0d4479-dc58-4719-886e-5ce610764305
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Encode, Encode method [Security], Encode method [Security],IX500DistinguishedName interface, IX500DistinguishedName interface [Security],Encode method, IX500DistinguishedName.Encode, IX500DistinguishedName::Encode, certenroll/IX500DistinguishedName::Encode, security.ix500distinguishedname_encode_method
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
 - IX500DistinguishedName.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX500DistinguishedName::Encode


## -description


The <b>Encode</b> method initializes the object from a string that contains a distinguished name. This method is web enabled.


## -parameters




### -param strName [in]

A <b>BSTR</b> variable that contains the string to encode.


### -param NameFlags [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379394(v=VS.85).aspx">X500NameFlags</a> enumeration value that specifies the format of the encoded value.

<div class="alert"><b>Note</b>  The following flags are set automatically:<ul>
<li>The default value specified in Certenroll.h is <b>XCN_CERT_NAME_STR_NONE</b>.</li>
<li>If you do not specify XCN_CERT_NAME_STR_FORWARD_FLAG, then XCN_CERT_NAME_STR_REVERSE_FLAG is automatically applied.</li>
<li>If you do not specify XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG, then XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG is automatically applied.</li>
<li>XCN_CERT_NAME_STR_ENABLE_PUNYCODE_FLAG is automatically set regardless of any other flag you specify.</li>
</ul>
</div>
<div> </div>

## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the encoded value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>strName</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></dt>
</dl>
</td>
<td width="60%">
The length, in characters of the <i>strName</i> parameter cannot exceed 64 * 1024.

</td>
</tr>
</table>
 




## -remarks



This method internally calls the CryptoAPI <a href="https://msdn.microsoft.com/en-us/library/Aa377160(v=VS.85).aspx">CertStrToName</a> function. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377056(v=VS.85).aspx">Name</a> property to retrieve the name as a null-terminated character string. Call the  <a href="https://msdn.microsoft.com/en-us/library/Aa377053(v=VS.85).aspx">EncodedName</a> property to retrieve a string containing an encoded name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377051(v=VS.85).aspx">IX500DistinguishedName</a>
 

 

