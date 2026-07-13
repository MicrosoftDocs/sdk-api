---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetStyleSimulations
title: IXpsOMGlyphs::GetStyleSimulations (xpsobjectmodel.h)
description: Gets the style simulations that will be applied when rendering the glyphs.
helpviewer_keywords: ["GetStyleSimulations","GetStyleSimulations method [XPS Documents and Packaging]","GetStyleSimulations method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetStyleSimulations method","IXpsOMGlyphs.GetStyleSimulations","IXpsOMGlyphs::GetStyleSimulations","xps.ixpsomglyphs_getstylesimulations","xpsobjectmodel/IXpsOMGlyphs::GetStyleSimulations"]
old-location: xps\ixpsomglyphs_getstylesimulations.htm
tech.root: xps
ms.assetid: 5678f67e-ed26-4846-b2f7-4e7f9690ca43
ms.date: 12/05/2018
ms.keywords: GetStyleSimulations, GetStyleSimulations method [XPS Documents and Packaging], GetStyleSimulations method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetStyleSimulations method, IXpsOMGlyphs.GetStyleSimulations, IXpsOMGlyphs::GetStyleSimulations, xps.ixpsomglyphs_getstylesimulations, xpsobjectmodel/IXpsOMGlyphs::GetStyleSimulations
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
 - IXpsOMGlyphs::GetStyleSimulations
 - xpsobjectmodel/IXpsOMGlyphs::GetStyleSimulations
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
 - IXpsOMGlyphs.GetStyleSimulations
---

# IXpsOMGlyphs::GetStyleSimulations


## -description

Gets the style simulations that will  be applied when rendering the glyphs.

## -parameters

### -param styleSimulations [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_style_simulation">XPS_STYLE_SIMULATION</a> value that describes the style simulations to be applied.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>styleSimulations</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_style_simulation">XPS_STYLE_SIMULATION</a>