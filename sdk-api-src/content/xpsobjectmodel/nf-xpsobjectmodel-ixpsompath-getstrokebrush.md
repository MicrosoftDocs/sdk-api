---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeBrush
title: IXpsOMPath::GetStrokeBrush (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets a pointer to the resolved IXpsOMBrush interface that contains the stroke brush that has been set for the path.
old-location: xps\ixpsompath_getstrokebrush.htm
tech.root: printdocs
ms.assetid: dbf786b0-5603-4735-8770-4c5e17a67253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStrokeBrush, GetStrokeBrush method [XPS Documents and Packaging], GetStrokeBrush method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeBrush method, IXpsOMPath.GetStrokeBrush, IXpsOMPath::GetStrokeBrush, xps.ixpsompath_getstrokebrush, xpsobjectmodel/IXpsOMPath::GetStrokeBrush
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMPath.GetStrokeBrush"
dev_langs:
 - c++
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
 - IXpsOMPath.GetStrokeBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath::GetStrokeBrush


## -description


Gets a pointer to the resolved <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the stroke brush that has been set for the path.


## -parameters




### -param brush [out, retval]

The stroke brush that has been set for the path. If a stroke brush has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the brush.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i></th>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>


</td>
<td>
The shared brush retrieved, with a lookup key that matches the key that is set by <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a> nor <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>brush</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> references an object that is not a brush.

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




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

