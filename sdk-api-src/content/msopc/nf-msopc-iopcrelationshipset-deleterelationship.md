---
UID: NF:msopc.IOpcRelationshipSet.DeleteRelationship
title: IOpcRelationshipSet::DeleteRelationship
author: windows-sdk-content
description: Deletes a specified IOpcRelationship interface pointer from the set.
old-location: opc\iopcrelationshipset_deleterelationship.htm
old-project: OPC
ms.assetid: fa452e8d-10dd-4cc4-a56b-a09d841dc46a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DeleteRelationship, DeleteRelationship method [Open Packaging Conventions], DeleteRelationship method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],DeleteRelationship method, IOpcRelationshipSet.DeleteRelationship, IOpcRelationshipSet::DeleteRelationship, msopc/IOpcRelationshipSet::DeleteRelationship, opc.iopcrelationshipset_deleterelationship
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - IOpcRelationshipSet.DeleteRelationship
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSet::DeleteRelationship


## -description


Deletes a specified <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer from the set.


## -parameters




### -param relationshipIdentifier [in]

The unique   identifier of a relationship.

The <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer to be deleted is the pointer to the relationship object that represents the relationship the  specified identifier.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_RELATIONSHIP</b></dt>
<dt>0x80510048</dt>
</dl>
</td>
<td width="60%">
The specified relationship does not exist.

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



When an  <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer is deleted from the set, the relationship it represents is not saved when the package is saved.


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
 

 

