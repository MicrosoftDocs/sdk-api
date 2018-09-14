---
UID: NF:msopc.IOpcRelationship.GetTargetUri
title: IOpcRelationship::GetTargetUri
author: windows-sdk-content
description: Gets the URI of the relationship&#160;target.
old-location: opc\iopcrelationship_gettargeturi.htm
tech.root: OPC
ms.assetid: 65b04931-dc4e-4eb5-b542-a7b46c3164de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetTargetUri, GetTargetUri method [Open Packaging Conventions], GetTargetUri method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetTargetUri method, IOpcRelationship.GetTargetUri, IOpcRelationship::GetTargetUri, msopc/IOpcRelationship::GetTargetUri, opc.iopcrelationship_gettargeturi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
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
 - IOpcRelationship.GetTargetUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationship::GetTargetUri


## -description


Gets the URI of the relationship target.


## -parameters




### -param targetUri [out, retval]

A pointer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a> interface of the URI that represents the URI of the relationship's target.

If the relationship target is internal, the  target is a part and the URI of the target is relative to the URI of the source part.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>targetUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The definitive way to find a part of interest is by using a relationship type.

Finding a part of interest requires several steps. For detailed information about finding a part, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a> and <a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a>.

To determine whether the target of the relationship is internal or external, call the <b>GetTargetUri</b> method.

If the relationship target is internal, the target is a part.

If the relationship target is a part, the URI in <i>targetUri</i> is relative to the URI of the relationship source.

If the relationship  target is a part, form the part name by calling the <a href="https://msdn.microsoft.com/9bb4c351-12ef-4e26-bcb1-59f81a413588">IOpcUri::CombinePartUri</a> method from the <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a> interface pointer received in <i>sourceUri</i> parameter of the <a href="https://msdn.microsoft.com/8e2587af-fce0-437a-9608-6824e861d699">GetSourceUri</a> method. Use the relative URI received in <i>targetUri</i> as the input parameter of the <b>IOpcUri::CombinePartUri</b> call. For an example, see <a href="https://msdn.microsoft.com/e95db16f-ac25-4936-babb-20f2afdd2f06">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/af052aa3-db7a-47de-938c-32895b8735e9">OPC_URI_TARGET_MODE</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>



<a href="https://msdn.microsoft.com/e95db16f-ac25-4936-babb-20f2afdd2f06">Resolving a Part Name from a Target URI</a>
 

 

