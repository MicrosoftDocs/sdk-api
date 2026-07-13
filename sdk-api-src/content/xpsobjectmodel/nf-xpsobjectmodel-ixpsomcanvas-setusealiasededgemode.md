---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetUseAliasedEdgeMode
title: IXpsOMCanvas::SetUseAliasedEdgeMode (xpsobjectmodel.h)
description: Sets the value that determines whether the edges of objects in this canvas will be rendered using the aliased edge mode.
helpviewer_keywords: ["FALSE","IXpsOMCanvas interface [XPS Documents and Packaging]","SetUseAliasedEdgeMode method","IXpsOMCanvas.SetUseAliasedEdgeMode","IXpsOMCanvas::SetUseAliasedEdgeMode","SetUseAliasedEdgeMode","SetUseAliasedEdgeMode method [XPS Documents and Packaging]","SetUseAliasedEdgeMode method [XPS Documents and Packaging]","IXpsOMCanvas interface","TRUE","xps.ixpsomcanvas_setusealiasededgemode","xpsobjectmodel/IXpsOMCanvas::SetUseAliasedEdgeMode"]
old-location: xps\ixpsomcanvas_setusealiasededgemode.htm
tech.root: xps
ms.assetid: a16b10fe-5065-4044-b632-452a79f61e90
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMCanvas interface [XPS Documents and Packaging],SetUseAliasedEdgeMode method, IXpsOMCanvas.SetUseAliasedEdgeMode, IXpsOMCanvas::SetUseAliasedEdgeMode, SetUseAliasedEdgeMode, SetUseAliasedEdgeMode method [XPS Documents and Packaging], SetUseAliasedEdgeMode method [XPS Documents and Packaging],IXpsOMCanvas interface, TRUE, xps.ixpsomcanvas_setusealiasededgemode, xpsobjectmodel/IXpsOMCanvas::SetUseAliasedEdgeMode
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
 - IXpsOMCanvas::SetUseAliasedEdgeMode
 - xpsobjectmodel/IXpsOMCanvas::SetUseAliasedEdgeMode
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
 - IXpsOMCanvas.SetUseAliasedEdgeMode
---

# IXpsOMCanvas::SetUseAliasedEdgeMode


## -description

Sets the value that determines whether the edges of objects in this canvas will be rendered using the aliased edge mode.

## -parameters

### -param useAliasedEdgeMode [in]

The Boolean value that determines whether  the edges of child objects in this canvas will be rendered using the aliased edge mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The edges of objects in the canvas are to be rendered without anti-aliasing using the aliased edge mode. This includes any objects that have this value set to <b>FALSE</b>.

In the document markup, this  corresponds  to the <b>RenderOptions.EdgeMode</b> attribute  having the value of <b>Aliased</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The edges of objects in the canvas are to be rendered in the default manner.

In the document markup, this corresponds  to the <b>RenderOptions.EdgeMode</b> attribute being absent.

</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This property corresponds to the <b>RenderOptions.EdgeMode</b> attribute of the <b>Canvas</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>