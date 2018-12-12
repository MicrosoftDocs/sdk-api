---
UID: NF:msopc.IOpcRelationship.GetId
title: IOpcRelationship::GetId
author: windows-sdk-content
description: Gets the unique identifier of the relationship.
old-location: opc\iopcrelationship_getid.htm
tech.root: OPC
ms.assetid: 8646d592-d568-4b82-80f3-2673cd0d2721
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetId, GetId method [Open Packaging Conventions], GetId method [Open Packaging Conventions],IOpcRelationship interface, IOpcRelationship interface [Open Packaging Conventions],GetId method, IOpcRelationship.GetId, IOpcRelationship::GetId, msopc/IOpcRelationship::GetId, opc.iopcrelationship_getid
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
 - IOpcRelationship.GetId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationship::GetId


## -description


Gets the unique identifier of the relationship.


## -parameters




### -param relationshipIdentifier [out, retval]

The identifier of the relationship.

The identifier of a relationship is arbitrary and local to the package, and, therefore, .

Valid identifiers conform to the restrictions for <b>xsd:ID</b>, which are  documented in section 3.3.8 ID of the <a href=" http://go.microsoft.com/fwlink/p/?linkid=126664">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a> (http://go.microsoft.com/fwlink/p/?linkid=126664).


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
The <i>relationshipIdentifier</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The identifier of a relationship is not useful for finding relationships because it is arbitrary and local to the package.

The definitive way to find a part of interest is by using a relationship type.

Finding a part requires several steps. For detailed information about finding a part, see <a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a>.

This method allocates memory used by the string returned in <i>relationshipIdentifier</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.

For more information about relationships, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>



<a href=" http://go.microsoft.com/fwlink/p/?linkid=126664">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a>
 

 

