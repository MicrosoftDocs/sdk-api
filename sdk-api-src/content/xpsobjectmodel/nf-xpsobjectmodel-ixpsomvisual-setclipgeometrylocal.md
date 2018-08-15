---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetClipGeometryLocal
title: IXpsOMVisual::SetClipGeometryLocal
author: windows-sdk-content
description: Sets the local, unshared clipping region for the visual.
old-location: xps\ixpsomvisual_setclipgeometrylocal.htm
old-project: printdocs
ms.assetid: 8b703866-9dc0-4327-9988-908f17bd4b21
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetClipGeometryLocal method, IXpsOMVisual.SetClipGeometryLocal, IXpsOMVisual::SetClipGeometryLocal, SetClipGeometryLocal, SetClipGeometryLocal method [XPS Documents and Packaging], SetClipGeometryLocal method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setclipgeometrylocal, xpsobjectmodel/IXpsOMVisual::SetClipGeometryLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMVisual.SetClipGeometryLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::SetClipGeometryLocal


## -description


Sets the local, unshared clipping region for the visual.


## -parameters




### -param clipGeometry [in]

A pointer to the  <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface to be set as the local, unshared clipping region for the visual. A <b>NULL</b> pointer releases the previously assigned geometry interface.


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
<i>clipGeometry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetClipGeometryLocal</b>, the clip geometry lookup key is released and <a href="https://msdn.microsoft.com/aa101ac6-65e8-4f6b-a6fa-59f3a003ffc5">GetClipGeometryLookup</a> returns a <b>NULL</b> pointer in the <i>key</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i>   by <a href="https://msdn.microsoft.com/f56fa077-749c-422b-b82d-161f9e5d4766">GetClipGeometry</a>
</th>
<th>Object that is returned in <i>clipGeometry</i> by <a href="https://msdn.microsoft.com/19efe0d7-6b11-41bc-80e7-e43e64d977b4">GetClipGeometryLocal</a>
</th>
<th>String that is returned in <i>key</i>  by <a href="https://msdn.microsoft.com/aa101ac6-65e8-4f6b-a6fa-59f3a003ffc5">GetClipGeometryLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetClipGeometryLocal</b> (this method)

</td>
<td>
The local clip geometry that is set by <b>SetClipGeometryLocal</b>.

</td>
<td>
The local clip geometry that is set by <b>SetClipGeometryLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>


</td>
<td>
The shared clip geometry that gets retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a> nor <b>SetClipGeometryLocal</b> has been called yet.

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




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

