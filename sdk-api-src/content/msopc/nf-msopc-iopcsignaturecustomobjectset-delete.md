---
UID: NF:msopc.IOpcSignatureCustomObjectSet.Delete
title: IOpcSignatureCustomObjectSet::Delete
author: windows-sdk-content
description: Deletes a specified IOpcSignatureCustomObject interface pointer from the set.
old-location: opc\iopcsignaturecustomobjectset_delete.htm
tech.root: OPC
ms.assetid: 7cfd8439-8f7e-4112-a2c0-3827922fb4b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Delete, Delete method [Open Packaging Conventions], Delete method [Open Packaging Conventions],IOpcSignatureCustomObjectSet interface, IOpcSignatureCustomObjectSet interface [Open Packaging Conventions],Delete method, IOpcSignatureCustomObjectSet.Delete, IOpcSignatureCustomObjectSet::Delete, msopc/IOpcSignatureCustomObjectSet::Delete, opc.iopcsignaturecustomobjectset_delete
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
req.idl: OpcDigitalSignature.idl
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
 - IOpcSignatureCustomObjectSet.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureCustomObjectSet::Delete


## -description


Deletes a specified <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer from the set.


## -parameters




### -param customObject [in]

An <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer to be deleted.


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
The <i>customObject</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When an <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer is deleted from the set, the <b>Object</b> it represents is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

