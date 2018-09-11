---
UID: NF:xpsobjectmodel.IXpsOMPath.GetGeometry
title: IXpsOMPath::GetGeometry
author: windows-sdk-content
description: Gets a pointer to the path's IXpsOMGeometry interface, which describes the resolved fill area for this path.
old-location: xps\ixpsompath_getgeometry.htm
tech.root: printdocs
ms.assetid: c4a99bf6-09d8-426a-8878-1126578c4518
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetGeometry, GetGeometry method [XPS Documents and Packaging], GetGeometry method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetGeometry method, IXpsOMPath.GetGeometry, IXpsOMPath::GetGeometry, xps.ixpsompath_getgeometry, xpsobjectmodel/IXpsOMPath::GetGeometry
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMPath.GetGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::GetGeometry


## -description


Gets a pointer to the path's <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface, which describes the  resolved fill area for this path.


## -parameters




### -param geometry [out, retval]

A pointer to the path's <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface, which describes the  resolved fill area for this path. If a geometry has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the geometry.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>geometry</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/32657c0d-3be5-466c-98a7-6bbd46f710d1">SetGeometryLocal</a>


</td>
<td>
The local geometry that is set by <a href="https://msdn.microsoft.com/32657c0d-3be5-466c-98a7-6bbd46f710d1">SetGeometryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>


</td>
<td>
The shared geometry retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/32657c0d-3be5-466c-98a7-6bbd46f710d1">SetGeometryLocal</a> nor <a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>geometry</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the lookup value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

