---
UID: NF:xpsobjectmodel.IXpsOMVisualBrush.GetVisualLookup
title: IXpsOMVisualBrush::GetVisualLookup (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the lookup key name of a visual in a resource dictionary; the visual is to be used as the source for the brush.
old-location: xps\ixpsomvisualbrush_getvisuallookup.htm
tech.root: printdocs
ms.assetid: 091cb7f3-6302-40a0-b509-c72e20109f75
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVisualLookup, GetVisualLookup method [XPS Documents and Packaging], GetVisualLookup method [XPS Documents and Packaging],IXpsOMVisualBrush interface, IXpsOMVisualBrush interface [XPS Documents and Packaging],GetVisualLookup method, IXpsOMVisualBrush.GetVisualLookup, IXpsOMVisualBrush::GetVisualLookup, xps.ixpsomvisualbrush_getvisuallookup, xpsobjectmodel/IXpsOMVisualBrush::GetVisualLookup
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMVisualBrush.GetVisualLookup"
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
 - IXpsOMVisualBrush.GetVisualLookup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMVisualBrush::GetVisualLookup


## -description


Gets the lookup key name of a visual in a resource dictionary; the visual is to be used as the source for the brush.


## -parameters




### -param lookup [out, retval]

The key name of a visual in a resource dictionary; the visual is  to be used as the source for the brush. If a visual's lookup key has not been set, or if a local visual has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>lookup</i></th>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallookup">SetVisualLookup</a>


</td>
<td>
The lookup key that is set by <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallookup">SetVisualLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallocal">SetVisualLocal</a> nor <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisualbrush-setvisuallookup">SetVisualLookup</a> has been called yet.

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
<i>lookup</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory used by the string that is returned in <i>lookup</i>.  If <i>lookup</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

