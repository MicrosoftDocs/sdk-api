---
UID: NF:certenc.ICertEncodeAltName.GetNameChoice
title: ICertEncodeAltName::GetNameChoice
author: windows-sdk-content
description: Returns the name choice at a specified index of an alternate name array.
old-location: security\icertencodealtname_getnamechoice.htm
tech.root: seccrypto
ms.assetid: 3b21fbc7-cba1-49b1-bad6-232f717e3056
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CCertEncodeAltName object [Security],GetNameChoice method, GetNameChoice, GetNameChoice method [Security], GetNameChoice method [Security],CCertEncodeAltName object, GetNameChoice method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],GetNameChoice method, ICertEncodeAltName.GetNameChoice, ICertEncodeAltName::GetNameChoice, _certsrv_icertencodealtname_getnamechoice, certenc/ICertEncodeAltName::GetNameChoice, security.icertencodealtname_getnamechoice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeAltName.GetNameChoice
 - CCertEncodeAltName.GetNameChoice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeAltName::GetNameChoice


## -description


The <b>GetNameChoice</b> method returns the name choice at a specified index of an alternate name array.


## -parameters




### -param NameIndex [in]

Specifies the index of the alternate name entry. The first entry is at index zero.


### -param pNameChoice [out]

A pointer to a <b>LONG</b> that receives the name choice specifier.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pNameChoice</i> parameter points to a value that indicates the type of the alternate name. This is one of the following values.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the name choice at the specified index. The name choice indicates the type of the alternate name so that it can be used correctly. It must be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_DIRECTORY_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is a directory name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_DNS_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string that contains a DNS (Domain Name System) name in the format <i>Host</i><b>.</b><i>Entity</i><b>.</b><i>Domain</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_IP_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The name is an octet string that represents an Internet protocol address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_REGISTERED_ID</b></dt>
</dl>
</td>
<td width="60%">
The name is a registered <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_RFC822_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name is an email address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_URL</b></dt>
</dl>
</td>
<td width="60%">
The name is an IA5 string that contains a URL in the format <i>Service</i><b>://</b><i>HostName</i><b>/</b><i>Path</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_ALT_NAME_OTHER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name consists of an OID and a binary <a href="https://msdn.microsoft.com/en-us/library/ms721569(v=VS.85).aspx">BLOB</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383295(v=VS.85).aspx">ICertEncodeAltName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383304(v=VS.85).aspx">ICertEncodeAltName::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383657(v=VS.85).aspx">ICertEncodeAltName::SetNameEntry</a>
 

 

