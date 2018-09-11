---
UID: NN:msopc.IOpcPartUri
title: IOpcPartUri
author: windows-sdk-content
description: Represents the part name of a part.
old-location: opc\iopcparturi.htm
tech.root: OPC
ms.assetid: 81123212-7a32-4833-b81f-8454a544327d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcPartUri, IOpcPartUri interface [Open Packaging Conventions], IOpcPartUri interface [Open Packaging Conventions],described, msopc/IOpcPartUri, opc.iopcparturi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcPartUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcPartUri interface


## -description


Represents the part name of a part.  If the part is a Relationships part, it is represented by the <a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a> interface; otherwise, it is represented by the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPartUri</b> interface inherits from <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a>. <b>IOpcPartUri</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPartUri</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b97890f8-dc9d-494f-82f9-3d32c09f5d67">ComparePartUri</a>
</td>
<td align="left" width="63%">
Returns an integer that indicates whether the URIs represented by the current part URI object and a specified part URI object are equivalent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02e8570b-3826-4619-b4f5-c1f74e27aefc">GetSourceUri</a>
</td>
<td align="left" width="63%">
              Gets  the source URI of the relationships that are stored in a  Relationships part. The  current part URI object represents the part name of that Relationships part.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11d271ab-247c-4060-b769-45e462b66255">IsRelationshipsPartUri</a>
</td>
<td align="left" width="63%">
Returns a value that indicates whether the current part URI object represents the part name of a Relationships part.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this interface is the same on all supported Windows versions. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8634d166-767a-46a5-9001-5fca88bfa844">IOpcFactory::CreatePartUri</a>



<a href="https://msdn.microsoft.com/83fed005-c061-4f1d-8b2b-73397e0b7a92">IOpcPart::GetName</a>



<a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

