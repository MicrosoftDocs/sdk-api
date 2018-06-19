---
UID: NN:certenc.ICertEncodeCRLDistInfo
title: ICertEncodeCRLDistInfo
author: windows-sdk-content
description: Provides methods for handling certificate revocation list (CRL) distribution information arrays used in certificate extensions.
old-location: security\icertencodecrldistinfo.htm
old-project: SecCrypto
ms.assetid: e9c0053f-263f-4d7b-9356-bc33af989dbe
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ICertEncodeCRLDistInfo, ICertEncodeCRLDistInfo interface [Security], ICertEncodeCRLDistInfo interface [Security],described, _certsrv_icertencodecrldistinfo, certenc/ICertEncodeCRLDistInfo, security.icertencodecrldistinfo
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeCRLDistInfo interface


## -description


The <b>ICertEncodeCRLDistInfo</b> interface provides methods for handling <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution information arrays used in certificate extensions.

 A certificate extension can be created by using a CRL distribution information array stored in an 
<a href="https://msdn.microsoft.com/a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b">extension handler</a> COM object instantiated by the policy module. Each element in the array is a CRL distribution point structure that contains an array of names and name choices. This interface is useful for encoding and decoding szOID_CRL_DIST_POINTS "2.5.29.31" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeCRLDistInfo</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeCRLDistInfo</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertEncodeCRLDistInfo</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertEncodeCRLDistInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3df104a5-fbd7-4eb1-a6b2-b3e51afa15bf">Decode</a>
</td>
<td align="left" width="63%">
Decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded CRL distribution information extension and stores the resulting array in the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46520e3a-1f15-4d1c-9f44-b9b420fb4f25">Encode</a>
</td>
<td align="left" width="63%">
Performs ASN.1 encoding on a CRL distribution information array stored in the COM object and returns the ASN.1-encoded extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c7d0d14-e755-4223-8cd5-0ebc784960cf">GetDistPointCount</a>
</td>
<td align="left" width="63%">
Returns the number of CRL distribution point elements in a CRL distribution information array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a564af61-fb5e-46b7-a818-333b4d5e2f25">GetName</a>
</td>
<td align="left" width="63%">
Returns the name at a specified index of a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cab5d4a0-e6dc-4229-a3b7-2dc90e2256bf">GetNameChoice</a>
</td>
<td align="left" width="63%">
Returns the name choice at a specified index of a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64102b89-defe-4f26-b6b2-8c3903e08347">GetNameCount</a>
</td>
<td align="left" width="63%">
Returns the number of names in a CRL distribution point structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets an array of CRL distribution information structures to a specified number of structures and clears the structure elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce27adfd-e21a-4e8d-882e-72041f97958a">SetNameCount</a>
</td>
<td align="left" width="63%">
Sets the name count for the specified distribution point in a CRL distribution information array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe33265a-8c75-4e16-8178-3569cf30d8e4">SetNameEntry</a>
</td>
<td align="left" width="63%">
Sets the name and name choice at a specified index of a distribution point in a CRL distribution information array.

</td>
</tr>
</table> 

