---
UID: NF:xpsobjectmodel.IXpsOMPath.SetGeometryLocal
title: IXpsOMPath::SetGeometryLocal (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the pointer to the local, unshared IXpsOMGeometry interface that contains the geometry of the resolved fill area to be set for this path.
old-location: xps\ixpsompath_setgeometrylocal.htm
tech.root: printdocs
ms.assetid: 32657c0d-3be5-466c-98a7-6bbd46f710d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetGeometryLocal method, IXpsOMPath.SetGeometryLocal, IXpsOMPath::SetGeometryLocal, SetGeometryLocal, SetGeometryLocal method [XPS Documents and Packaging], SetGeometryLocal method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setgeometrylocal, xpsobjectmodel/IXpsOMPath::SetGeometryLocal
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMPath.SetGeometryLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::SetGeometryLocal


## -description


Sets the pointer to the local, unshared <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the  geometry of the resolved fill area to be set for this path.


## -parameters




### -param geometry [in]

The pointer to the local, unshared <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the  geometry of the resolved fill area to be set for this path.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>geometry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetGeometryLocal</b>, the geometry lookup key is released and <a href="https://msdn.microsoft.com/f40b6ed0-6e75-4f0a-abcc-f13d961df678">GetGeometryLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>geometry</i> by <a href="https://msdn.microsoft.com/c4a99bf6-09d8-426a-8878-1126578c4518">GetGeometry</a>
</th>
<th>Object that is returned in <i>geometry</i> by <a href="https://msdn.microsoft.com/a8902191-7646-4c97-843f-9467ed12f621">GetGeometryLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/f40b6ed0-6e75-4f0a-abcc-f13d961df678">GetGeometryLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetGeometryLocal</b> (this method)

</td>
<td>
The local geometry that is set by <b>SetGeometryLocal</b>.

</td>
<td>
The local geometry that is set by <b>SetGeometryLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>


</td>
<td>
The shared geometry retrieved, with a lookup key that matches the key set by <a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetGeometryLocal</b> nor <a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

