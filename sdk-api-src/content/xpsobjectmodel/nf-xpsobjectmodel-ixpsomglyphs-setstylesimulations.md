---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetStyleSimulations
title: IXpsOMGlyphs::SetStyleSimulations (xpsobjectmodel.h)
description: Sets the style simulations that will be applied when the glyphs are rendered.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetStyleSimulations method","IXpsOMGlyphs.SetStyleSimulations","IXpsOMGlyphs::SetStyleSimulations","SetStyleSimulations","SetStyleSimulations method [XPS Documents and Packaging]","SetStyleSimulations method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setstylesimulations","xpsobjectmodel/IXpsOMGlyphs::SetStyleSimulations"]
old-location: xps\ixpsomglyphs_setstylesimulations.htm
tech.root: xps
ms.assetid: 2b87f12c-5d9b-47ea-99f0-e457c3e49c92
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetStyleSimulations method, IXpsOMGlyphs.SetStyleSimulations, IXpsOMGlyphs::SetStyleSimulations, SetStyleSimulations, SetStyleSimulations method [XPS Documents and Packaging], SetStyleSimulations method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setstylesimulations, xpsobjectmodel/IXpsOMGlyphs::SetStyleSimulations
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGlyphs::SetStyleSimulations
 - xpsobjectmodel/IXpsOMGlyphs::SetStyleSimulations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphs.SetStyleSimulations
---

# IXpsOMGlyphs::SetStyleSimulations


## -description

Sets the style simulations that will be applied when the glyphs are rendered.

## -parameters

### -param styleSimulations [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_style_simulation">XPS_STYLE_SIMULATION</a> value that specifies the style simulation to be applied.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>styleSimulations</i> is not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_style_simulation">XPS_STYLE_SIMULATION</a> value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_style_simulation">XPS_STYLE_SIMULATION</a>