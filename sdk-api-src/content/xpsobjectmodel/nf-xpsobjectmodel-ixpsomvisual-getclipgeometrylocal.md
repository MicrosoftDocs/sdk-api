---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetClipGeometryLocal
title: IXpsOMVisual::GetClipGeometryLocal
author: windows-sdk-content
description: Gets a pointer to the IXpsOMGeometry interface that contains the local, unshared geometry of the visual's clipping region.
old-location: xps\ixpsomvisual_getclipgeometrylocal.htm
tech.root: printdocs
ms.assetid: 19efe0d7-6b11-41bc-80e7-e43e64d977b4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetClipGeometryLocal, GetClipGeometryLocal method [XPS Documents and Packaging], GetClipGeometryLocal method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetClipGeometryLocal method, IXpsOMVisual.GetClipGeometryLocal, IXpsOMVisual::GetClipGeometryLocal, xps.ixpsomvisual_getclipgeometrylocal, xpsobjectmodel/IXpsOMVisual::GetClipGeometryLocal
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
 - IXpsOMVisual.GetClipGeometryLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisual::GetClipGeometryLocal


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the local, unshared geometry of the visual's clipping region.


## -parameters




### -param clipGeometry [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the local, unshared geometry of the visual's clipping region. If a clip geometry lookup key has been set, or if a local clip geometry has not been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a>


</td>
<td>
The local clip geometry that is set by <a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a> nor <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a> has been called yet.

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
<i>clipGeometry</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

