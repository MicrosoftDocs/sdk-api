---
UID: NN:certenc.ICertEncodeBitString
title: ICertEncodeBitString
author: windows-sdk-content
description: Provides methods for handling bit strings used in certificate extensions.
old-location: security\icertencodebitstring.htm
tech.root: seccrypto
ms.assetid: 51178b67-46da-49f8-9bd7-a500e846e0a8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertEncodeBitString, ICertEncodeBitString interface [Security], ICertEncodeBitString interface [Security],described, _certsrv_icertencodebitstring, certenc/ICertEncodeBitString, security.icertencodebitstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ICertEncodeBitString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeBitString interface


## -description


The <b>ICertEncodeBitString</b> interface provides methods for handling bit strings used in certificate extensions. A certificate extension can be created by using a bit string stored in an 
<a href="https://msdn.microsoft.com/en-us/library/Aa388215(v=VS.85).aspx">extension handler</a> COM object instantiated by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa387348(v=VS.85).aspx">policy module</a>. The bit string can contain an arbitrary string of binary values. This interface is useful for encoding and decoding szOID_KEY_USAGE "2.5.29.15" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeBitString</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeBitString</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeBitString</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertEncodeBitString</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeBitString</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383873(v=VS.85).aspx">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1)-encoded bit string and stores the resulting bit string in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383878(v=VS.85).aspx">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a bit string and returns the ASN.1-encoded bit string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383893(v=VS.85).aspx">GetBitCount</a>
</td>
<td align="left" width="63%">
Returns the number of bits in a bit string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383899(v=VS.85).aspx">GetBitString</a>
</td>
<td align="left" width="63%">
Returns the bit string.

</td>
</tr>
</table> 

