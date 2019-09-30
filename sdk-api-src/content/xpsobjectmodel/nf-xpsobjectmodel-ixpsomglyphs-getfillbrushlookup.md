---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFillBrushLookup
title: IXpsOMGlyphs::GetFillBrushLookup (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the lookup key of the IXpsOMBrush interface that is stored in a resource dictionary and will be used as the fill brush.
old-location: xps\ixpsomglyphs_getfillbrushlookup.htm
tech.root: printdocs
ms.assetid: f71b0b98-12d6-4108-8b1e-4ad254ffbdfd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFillBrushLookup, GetFillBrushLookup method [XPS Documents and Packaging], GetFillBrushLookup method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFillBrushLookup method, IXpsOMGlyphs.GetFillBrushLookup, IXpsOMGlyphs::GetFillBrushLookup, xps.ixpsomglyphs_getfillbrushlookup, xpsobjectmodel/IXpsOMGlyphs::GetFillBrushLookup
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMGlyphs.GetFillBrushLookup"
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
 - IXpsOMGlyphs.GetFillBrushLookup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphs::GetFillBrushLookup


## -description


Gets the lookup key of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that is stored in a resource dictionary and will be used as the fill brush.


## -parameters




### -param key [out, retval]

The lookup key for the brush that is stored in a resource dictionary and will be used as the fill brush. If a fill brush lookup key has not been set or if a local fill brush has been set, a <b>NULL</b> pointer will be returned.

<table>
<tr>
<th>Most recent method called</th>
<th>String that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlookup">SetFillBrushLookup</a>


</td>
<td>
The lookup key that is set by <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlookup">SetFillBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlocal">SetFillBrushLocal</a> nor <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-setfillbrushlookup">SetFillBrushLookup</a> has been called yet.

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
<i>key</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates the memory that is used by the string returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

