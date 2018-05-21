---
UID: NN:certenc.ICertEncodeAltName
title: ICertEncodeAltName
author: windows-driver-content
description: Provides methods for handling alternate names used in certificate extensions.
old-location: security\icertencodealtname.htm
old-project: SecCrypto
ms.assetid: e0ecfcb0-f2ca-4e1c-a054-c83c03d55465
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ICertEncodeAltName, ICertEncodeAltName interface [Security], ICertEncodeAltName interface [Security],described, _certsrv_icertencodealtname, certenc/ICertEncodeAltName, security.icertencodealtname
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenc.dll
api_name:
-	ICertEncodeAltName
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeAltName interface


## -description


The <b>ICertEncodeAltName</b> interface provides methods for handling alternate names used in certificate extensions.

A certificate extension can be created using an alternate name array stored in an 
<a href="https://msdn.microsoft.com/a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b">extension handler</a> COM object. Each element in the array is a structure that contains a name string and a name choice.

This interface is useful for encoding and decoding szOID_SUBJECT_ALT_NAME2 "2.5.29.17" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeAltName</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeAltName</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeAltName</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertEncodeAltName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeAltName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0507d3a5-b8c3-4f2e-996f-e1e32957f475">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded alternate name extension and stores the resulting array of strings in the extension handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34136053-1c25-4f6b-8bd6-699fffb6670b">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on an alternate name array stored in the extension handler and returns the name array as an array of ASN.1-encoded strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a3f36b-1c09-4b2e-84b7-a725d366fd77">GetName</a>
</td>
<td align="left" width="63%">
Returns the alternate name at a specified index of an alternate name array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b21fbc7-cba1-49b1-bad6-232f717e3056">GetNameChoice</a>
</td>
<td align="left" width="63%">
Returns a name choice at a specified index of an alternate name array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f5e5c5d-e21b-452b-837c-5b44daa884b8">GetNameCount</a>
</td>
<td align="left" width="63%">
Returns the count of names in an alternate name array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets an alternate name array to a specified number of elements and clears the values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">SetNameEntry</a>
</td>
<td align="left" width="63%">
Sets a name and name choice at a specified index of an alternate name array.

</td>
</tr>
</table> 

