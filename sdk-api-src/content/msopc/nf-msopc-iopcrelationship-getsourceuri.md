---
UID: NF:msopc.IOpcRelationship.GetSourceUri
title: IOpcRelationship::GetSourceUri (msopc.h)
author: windows-sdk-content
description: Gets the URI of the relationship&#160;source.
old-location: opc\iopcrelationship_getsourceuri.htm
tech.root: OPC
ms.assetid: 8e2587af-fce0-437a-9608-6824e861d699
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSourceUri, GetSourceUri method [Open Packaging Conventions], GetSourceUri method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetSourceUri method, IOpcRelationship.GetSourceUri, IOpcRelationship::GetSourceUri, msopc/IOpcRelationship::GetSourceUri, opc.iopcrelationship_getsourceuri
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
 - IOpcRelationship.GetSourceUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationship::GetSourceUri


## -description


Gets the URI of the relationship source.


## -parameters




### -param sourceUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a> interface of the OPC URI object that represents the URI of the relationship source.


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
The <i>sourceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If the source of a relationship is the package itself, the URI in <i>sourceUri</i> represents the package root: "/".

If the relationship  target is a part, form the part name by calling the <a href="https://msdn.microsoft.com/9bb4c351-12ef-4e26-bcb1-59f81a413588">IOpcUri::CombinePartUri</a> method from the <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a> interface pointer received in <i>sourceUri</i>. Use the relative URI received in the <i>targetUri</i> parameter of the <a href="https://msdn.microsoft.com/65b04931-dc4e-4eb5-b542-a7b46c3164de">GetTargetUri</a> method as the input parameter of the <b>IOpcUri::CombinePartUri</b> call. For an example, see <a href="https://msdn.microsoft.com/e95db16f-ac25-4936-babb-20f2afdd2f06">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>



<a href="https://msdn.microsoft.com/e95db16f-ac25-4936-babb-20f2afdd2f06">Resolving a Part Name from a Target URI</a>
 

 

