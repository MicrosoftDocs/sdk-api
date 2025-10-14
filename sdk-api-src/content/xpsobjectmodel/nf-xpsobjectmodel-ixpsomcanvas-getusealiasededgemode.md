---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetUseAliasedEdgeMode
title: IXpsOMCanvas::GetUseAliasedEdgeMode (xpsobjectmodel.h)
description: Gets a Boolean value that determines whether the edges of the objects in the canvas are to be rendered using the aliased edge mode.
helpviewer_keywords: ["FALSE","GetUseAliasedEdgeMode","GetUseAliasedEdgeMode method [XPS Documents and Packaging]","GetUseAliasedEdgeMode method [XPS Documents and Packaging]","IXpsOMCanvas interface","IXpsOMCanvas interface [XPS Documents and Packaging]","GetUseAliasedEdgeMode method","IXpsOMCanvas.GetUseAliasedEdgeMode","IXpsOMCanvas::GetUseAliasedEdgeMode","TRUE","xps.ixpsomcanvas_getusealiasededgemode","xpsobjectmodel/IXpsOMCanvas::GetUseAliasedEdgeMode"]
old-location: xps\ixpsomcanvas_getusealiasededgemode.htm
tech.root: xps
ms.assetid: 9d3f0660-227a-4b0f-bd41-112bd89e4605
ms.date: 12/05/2018
ms.keywords: FALSE, GetUseAliasedEdgeMode, GetUseAliasedEdgeMode method [XPS Documents and Packaging], GetUseAliasedEdgeMode method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetUseAliasedEdgeMode method, IXpsOMCanvas.GetUseAliasedEdgeMode, IXpsOMCanvas::GetUseAliasedEdgeMode, TRUE, xps.ixpsomcanvas_getusealiasededgemode, xpsobjectmodel/IXpsOMCanvas::GetUseAliasedEdgeMode
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
 - IXpsOMCanvas::GetUseAliasedEdgeMode
 - xpsobjectmodel/IXpsOMCanvas::GetUseAliasedEdgeMode
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
 - IXpsOMCanvas.GetUseAliasedEdgeMode
---

# IXpsOMCanvas::GetUseAliasedEdgeMode


## -description

Gets a Boolean value that determines whether the edges of the objects in the canvas are to be rendered using the aliased edge mode.

## -parameters

### -param useAliasedEdgeMode [out, retval]

The Boolean value that determines whether the objects in the canvas are to be rendered  using the aliased edge mode.

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
The edges of objects in the canvas are to be rendered without anti-aliasing using the aliased edge mode. This includes any objects in the canvas that have <i>useAliasedEdgeMode</i> set to <b>FALSE</b>.

In the document markup, this  corresponds  to the <b>RenderOptions.EdgeMode</b> attribute  having a value of <b>Aliased</b>.

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
<i>useAliasedEdgeMode</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property that is returned by this method corresponds to the <b>RenderOptions.EdgeMode</b> attribute of the <b>Canvas</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>