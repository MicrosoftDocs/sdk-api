---
UID: NF:certenc.ICertEncodeCRLDistInfo.GetNameChoice
title: ICertEncodeCRLDistInfo::GetNameChoice
author: windows-sdk-content
description: Returns the name choice at a specified index of a certificate revocation list (CRL) distribution information point.
old-location: security\icertencodecrldistinfo_getnamechoice.htm
tech.root: seccrypto
ms.assetid: cab5d4a0-e6dc-4229-a3b7-2dc90e2256bf
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],GetNameChoice method, GetNameChoice, GetNameChoice method [Security], GetNameChoice method [Security],CCertEncodeCRLDistInfo object, GetNameChoice method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],GetNameChoice method, ICertEncodeCRLDistInfo.GetNameChoice, ICertEncodeCRLDistInfo::GetNameChoice, _certsrv_icertencodecrldistinfo_getnamechoice, certenc/ICertEncodeCRLDistInfo::GetNameChoice, security.icertencodecrldistinfo_getnamechoice
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
 - ICertEncodeCRLDistInfo.GetNameChoice
 - CCertEncodeCRLDistInfo.GetNameChoice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeCRLDistInfo::GetNameChoice


## -description


The <b>GetNameChoice</b> method returns the name choice at a specified index of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information point.


## -parameters




### -param DistPointIndex [in]

Specifies the index of the distribution point for which to get a name choice. The first value is at index zero.


### -param NameIndex [in]

Specifies the index of the name choice entry to get. The first value is at index zero.


### -param pNameChoice [out]

A pointer to a <b>Long</b> that represents the name choice.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the name choice at the specified index. The name choice indicates the type of the name so that it can be used correctly. The name choice must be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>CERT_ALT_NAME_REGISTERED_ID</b></dt>
</dl>
</td>
<td width="60%">
The name is a registered <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e9c0053f-263f-4d7b-9356-bc33af989dbe">ICertEncodeCRLDistInfo</a>



<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">ICertEncodeCRLDistInfo::SetNameEntry</a>
 

 

