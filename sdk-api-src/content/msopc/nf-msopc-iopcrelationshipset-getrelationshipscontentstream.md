---
UID: NF:msopc.IOpcRelationshipSet.GetRelationshipsContentStream
title: IOpcRelationshipSet::GetRelationshipsContentStream
author: windows-sdk-content
description: Gets a read-only stream that contains the part content of the Relationships part represented by the set.
old-location: opc\iopcrelationshipset_getrelationshipscontentstream.htm
old-project: OPC
ms.assetid: 648e5bd1-25cc-48df-8120-ca1756eff8f7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetRelationshipsContentStream, GetRelationshipsContentStream method [Open Packaging Conventions], GetRelationshipsContentStream method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],GetRelationshipsContentStream method, IOpcRelationshipSet.GetRelationshipsContentStream, IOpcRelationshipSet::GetRelationshipsContentStream, msopc/IOpcRelationshipSet::GetRelationshipsContentStream, opc.iopcrelationshipset_getrelationshipscontentstream
ms.prod: windows
ms.technology: windows-sdk
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
 - IOpcRelationshipSet.GetRelationshipsContentStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSet::GetRelationshipsContentStream


## -description


            Gets a read-only stream that contains the part content of the Relationships part represented by the set.


## -parameters




### -param contents [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the read-only  stream that contains the part content of the Relationships part represented by the set.

If  the relationships stored in the  Relationships part  have not been  modified, part content can include markup compatibility data that is not otherwise accessible through the relationship objects in the set.


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
The <i>contents</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/0ad335ff-57da-4d4a-95c0-6b9b513a9698">Package Consumption Error Group</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/877447bb-d4e1-4277-b8ce-cb7a31a33fe0">Part URI Error Group</a>. 

</td>
</tr>
</table>
 




## -remarks



Calling this method will parse and validate all the relationships in the relationships markup. If the Relationships part contains invalid relationships markup, the markup cannot be retrieved by this method.

For more information about markup compatibility and packages, see Part 5: Markup Compatibility in <a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a> (http://go.microsoft.com/fwlink/p/?linkid=123375).


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>
 

 

