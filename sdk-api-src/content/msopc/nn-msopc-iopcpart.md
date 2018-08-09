---
UID: NN:msopc.IOpcPart
title: IOpcPart
author: windows-sdk-content
description: Represents a part that contains data and is not a Relationships part.
old-location: opc\iopcpart.htm
old-project: OPC
ms.assetid: e6a40f30-03d1-4c93-a5e0-563b4c6588b4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcPart, IOpcPart interface [Open Packaging Conventions], IOpcPart interface [Open Packaging Conventions],described, msopc/IOpcPart, opc.iopcpart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcPart
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPart interface


## -description


Represents a part that contains data and is not a Relationships part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPart</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcPart</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPart</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aee8e3a2-3fac-40da-bea2-1fd4e2224c81">GetCompressionOptions</a>
</td>
<td align="left" width="63%">
Gets a value that describes the way part content is compressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b40e3df2-e717-465d-8893-511e4776d80d">GetContentStream</a>
</td>
<td align="left" width="63%">
Gets a stream that provides read/write access to  part content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe0d6ba3-8c62-4269-86ff-669609529933">GetContentType</a>
</td>
<td align="left" width="63%">
Gets the media  type of part content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83fed005-c061-4f1d-8b2b-73397e0b7a92">GetName</a>
</td>
<td align="left" width="63%">
Gets a part URI object that represents the part name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8a8ce1f-3420-457f-b02a-5dc3e9725a02">GetRelationshipSet</a>
</td>
<td align="left" width="63%">
Gets a relationship set object that represents the Relationships part that stores relationships that have the part as their source.

</td>
</tr>
</table> 


## -remarks



To create a part object to represent a part, call the <a href="https://msdn.microsoft.com/8c5de7ac-f51c-42f2-9068-8e9ede86ad97">IOpcPartSet::CreatePart</a> method. To get a pointer to the interface of a part object that represents an existing part, call the <a href="https://msdn.microsoft.com/3a44725b-23a0-4338-b618-c0ce4ecde204">IOpcPartSet::GetPart</a> or  <a href="https://msdn.microsoft.com/54759fcb-858f-434c-92e9-6164f3d972fb">IOpcPartEnumerator::GetCurrent</a> method.

A Relationships part cannot be represented by an implementation of the <b>IOpcPart</b> interface.

Methods of an <b>IOpcPart</b> interface provide access to part information through the properties listed in the following table:

<table>
<tr>
<th>Method</th>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/aee8e3a2-3fac-40da-bea2-1fd4e2224c81">GetCompressionOptions</a>
</td>
<td>Compression </td>
<td>
The compression option to be used on part content.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b40e3df2-e717-465d-8893-511e4776d80d">GetContentStream</a>
</td>
<td>Content</td>
<td>
The stream of bytes that makes up the part as described in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fe0d6ba3-8c62-4269-86ff-669609529933">GetContentType</a>
</td>
<td>Content type</td>
<td>
The media type of the part content, as specified by the package designer in compliance with the rules in the <i>OPC</i>.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/83fed005-c061-4f1d-8b2b-73397e0b7a92">GetName</a>
</td>
<td>Name</td>
<td>
The URI of the part in the package. 

</td>
</tr>
</table>
 

For more information about parts, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/f34c682f-7677-4d20-bd37-b1a68293d85c">IOpcPartSet</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>



<a href="https://msdn.microsoft.com/bc821e84-fd18-449c-89d0-a261f43f8971">OPC_COMPRESSION_OPTIONS</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<b>Reference</b>
 

 

