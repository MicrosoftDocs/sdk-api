---
UID: NN:msopc.IOpcPackage
title: IOpcPackage
author: windows-driver-content
description: Represents a package and provides methods to access the package's parts and relationships.
old-location: opc\iopcpackage.htm
old-project: OPC
ms.assetid: e7052dd2-c910-41d8-a58a-8f3e68e09dd0
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcPackage, IOpcPackage interface [Open Packaging Conventions], IOpcPackage interface [Open Packaging Conventions],described, msopc/IOpcPackage, opc.iopcpackage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPackage interface


## -description


Represents a package and provides methods to access the package's parts and relationships.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPackage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcPackage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPackage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9460e057-8fe8-46b8-b12e-ba761fcaf49b">GetPartSet</a>
</td>
<td align="left" width="63%">
Gets a part set object that contains <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointers. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/316fe21c-675a-47ec-b17e-0fe505a06c7f">GetRelationshipSet</a>
</td>
<td align="left" width="63%">
Gets a relationship set object that represents the Relationships part that stores package relationships.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call either the <a href="https://msdn.microsoft.com/9cd4ef3a-f890-40d5-a398-cb8f9746c380">IOpcFactory::CreatePackage</a> or <a href="https://msdn.microsoft.com/227a2724-c2b3-4f12-8d30-1ff1eca59c83">IOpcFactory::ReadPackageFromStream</a> method.

Package relationships serve as an entry point  to the package by  links from the package to target  resources. The target of a package relationship is often an important part described in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i> or by the package format designer.

For example, a package relationship can provide access to the Core Properties part that stores package metadata, or to a part containing format-specific data, where the part and data are described by the package designer.  The Main Document part of the word processing OpenXML format is one such format-specific part. For more information about this part, see Part 1: Fundamentals in <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a> (http://go.microsoft.com/fwlink/p/?linkid=123375).

The definitive way to find a part of interest is by using a relationship type. Several steps are required; for details, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a> and the <a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a> how-to task.

For more information about packages, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<a href="https://msdn.microsoft.com/f34c682f-7677-4d20-bd37-b1a68293d85c">IOpcPartSet</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/f42a8581-dcaa-43a6-997f-984303a32ff3">Packages Overview</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<b>Reference</b>
 

 

