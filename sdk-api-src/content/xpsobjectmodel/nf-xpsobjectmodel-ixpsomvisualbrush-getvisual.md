---
UID: NF:xpsobjectmodel.IXpsOMVisualBrush.GetVisual
title: IXpsOMVisualBrush::GetVisual
author: windows-sdk-content
description: Gets a pointer to the interface of the resolved visual to be used as the source for the brush.
old-location: xps\ixpsomvisualbrush_getvisual.htm
tech.root: printdocs
ms.assetid: b8fb6698-8ce7-42a1-bad6-bde3d5dbbbf8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetVisual, GetVisual method [XPS Documents and Packaging], GetVisual method [XPS Documents and Packaging],IXpsOMVisualBrush interface, IXpsOMVisualBrush interface [XPS Documents and Packaging],GetVisual method, IXpsOMVisualBrush.GetVisual, IXpsOMVisualBrush::GetVisual, xps.ixpsomvisualbrush_getvisual, xpsobjectmodel/IXpsOMVisualBrush::GetVisual
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
 - IXpsOMVisualBrush.GetVisual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMVisualBrush.GetVisual
: 
---

# IXpsOMVisualBrush::GetVisual


## -description


Gets a pointer to the interface of the resolved visual to be used as the source for the brush.


## -parameters




### -param visual [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface of the resolved visual object used as the source for the brush. If a visual has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently  been called to set the visual object.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>visual</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8ef37838-ff5f-4c8f-9fa3-30d11417c09d">SetVisualLocal</a>


</td>
<td>
The visual that is set by <a href="https://msdn.microsoft.com/8ef37838-ff5f-4c8f-9fa3-30d11417c09d">SetVisualLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>


</td>
<td>
The visual that is retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/8ef37838-ff5f-4c8f-9fa3-30d11417c09d">SetVisualLocal</a> nor <a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a> has been called yet.

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
<i>visual</i> is <b>NULL</b>.

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
 




## -remarks



This method returns an  <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface pointer. However, the  
	 interface that is returned can be any interface that inherits from   <b>IXpsOMVisual</b>, such as  <a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>, <a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>, 
	  and <a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/56c11e64-64a8-4c42-9547-4f1fcdc13a4b">IXpsOMVisualBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

