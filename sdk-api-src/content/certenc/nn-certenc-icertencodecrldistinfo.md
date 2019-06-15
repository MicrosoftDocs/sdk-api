---
UID: NN:certenc.ICertEncodeCRLDistInfo
title: ICertEncodeCRLDistInfo (certenc.h)
author: windows-sdk-content
description: Provides methods for handling certificate revocation list (CRL) distribution information arrays used in certificate extensions.
old-location: security\icertencodecrldistinfo.htm
tech.root: SecCrypto
ms.assetid: e9c0053f-263f-4d7b-9356-bc33af989dbe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertEncodeCRLDistInfo, ICertEncodeCRLDistInfo interface [Security], ICertEncodeCRLDistInfo interface [Security],described, _certsrv_icertencodecrldistinfo, certenc/ICertEncodeCRLDistInfo, security.icertencodecrldistinfo
ms.topic: interface
f1_keywords: ["certenc/ICertEncodeCRLDistInfo"]
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
 - ICertEncodeCRLDistInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertEncodeCRLDistInfo interface


## -description


The <b>ICertEncodeCRLDistInfo</b> interface provides methods for handling <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information arrays used in certificate extensions.

 A certificate extension can be created by using a CRL distribution information array stored in an 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object instantiated by the policy module. Each element in the array is a CRL distribution point structure that contains an array of names and name choices. This interface is useful for encoding and decoding szOID_CRL_DIST_POINTS "2.5.29.31" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeCRLDistInfo</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeCRLDistInfo</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeCRLDistInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeCRLDistInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertEncodeCRLDistInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-decode">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded CRL distribution information extension and stores the resulting array in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-encode">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a CRL distribution information array stored in the COM object and returns the ASN.1-encoded extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getdistpointcount">GetDistPointCount</a>
</td>
<td align="left" width="63%">
Returns the number of CRL distribution point elements in a CRL distribution information array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getname">GetName</a>
</td>
<td align="left" width="63%">
Returns the name at a specified index of a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getnamechoice">GetNameChoice</a>
</td>
<td align="left" width="63%">
Returns the name choice at a specified index of a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-getnamecount">GetNameCount</a>
</td>
<td align="left" width="63%">
Returns the number of names in a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets an array of CRL distribution information structures to a specified number of structures and clears the structure elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnamecount">SetNameCount</a>
</td>
<td align="left" width="63%">
Sets the name count for the specified distribution point in a CRL distribution information array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnameentry">SetNameEntry</a>
</td>
<td align="left" width="63%">
Sets the name and name choice at a specified index of a distribution point in a CRL distribution information array.

</td>
</tr>
</table> 

