---
UID: NN:msopc.IOpcPartSet
title: IOpcPartSet
author: windows-sdk-content
description: An unordered set of IOpcPart interface pointers to part objects that represent the parts in a package that are not Relationships parts.
old-location: opc\iopcpartset.htm
old-project: OPC
ms.assetid: f34c682f-7677-4d20-bd37-b1a68293d85c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcPartSet, IOpcPartSet interface [Open Packaging Conventions], IOpcPartSet interface [Open Packaging Conventions],described, msopc/IOpcPartSet, opc.iopcpartset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - IOpcPartSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPartSet interface


## -description


An unordered set of <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointers to part objects that represent the parts in a package that are not Relationships parts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPartSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcPartSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPartSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c5de7ac-f51c-42f2-9068-8e9ede86ad97">CreatePart</a>
</td>
<td align="left" width="63%">
Creates a part object that represents a part and adds a pointer to the object's <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface to the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d69530f-7e10-409a-8832-f410d6f9582e">DeletePart</a>
</td>
<td align="left" width="63%">
Deletes the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer of a specified part object from the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b2a5ae6-b3ac-49b5-a798-9fca450da6d1">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointers  in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a44725b-23a0-4338-b618-c0ce4ecde204">GetPart</a>
</td>
<td align="left" width="63%">
Gets a part object, which represents a specified part, in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/721e0252-330a-4218-9267-b3dd0dea7598">PartExists</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether a specified part is represented as a part object in the set.

</td>
</tr>
</table> 


## -remarks



To retrieve the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer of the part object that represents a specific part, call the <a href="https://msdn.microsoft.com/721e0252-330a-4218-9267-b3dd0dea7598">PartExists</a> method and pass in the part name to confirm that the part is represented in the set. If it is, call the <a href="https://msdn.microsoft.com/3a44725b-23a0-4338-b618-c0ce4ecde204">GetPart</a> method and pass in the part name to retrieve the <b>IOpcPart</b> interface pointer.

The <a href="https://msdn.microsoft.com/8c5de7ac-f51c-42f2-9068-8e9ede86ad97">CreatePart</a> method cannot create a part object that represents a Relationships part.

When a package that is represented as a package object is serialized, only the parts that are represented by part objects with <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointers included in the set are serialized with the package.

If a part is not represented by a part object in the set when the package is serialized, that part will not be serialized with the package.

When a part object is created and a pointer to it is added to the set, the part it represents is serialized when the package is serialized.

When an  <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer is deleted from the set, the part it represents is not serialized when the package is serialized.

An <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> provides access to the properties of the part. For details about these properties, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a> and <b>IOpcPart</b>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a2296b2-a149-439a-abcf-2bc2eb6d1235">IOpcPartEnumerator</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<b>Reference</b>
 

 

