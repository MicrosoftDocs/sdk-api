---
UID: NF:strmif.IGraphBuilder.Connect
title: IGraphBuilder::Connect (strmif.h)
description: The Connect method connects the two pins, using intermediates if necessary.
helpviewer_keywords: ["Connect","Connect method [DirectShow]","Connect method [DirectShow]","IGraphBuilder interface","IGraphBuilder interface [DirectShow]","Connect method","IGraphBuilder.Connect","IGraphBuilder::Connect","IGraphBuilderConnect","dshow.igraphbuilder_connect","strmif/IGraphBuilder::Connect"]
old-location: dshow\igraphbuilder_connect.htm
tech.root: dshow
ms.assetid: 8ddcbb73-8220-4d70-9ab3-58d99fa8a958
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [DirectShow], Connect method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],Connect method, IGraphBuilder.Connect, IGraphBuilder::Connect, IGraphBuilderConnect, dshow.igraphbuilder_connect, strmif/IGraphBuilder::Connect
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphBuilder::Connect
 - strmif/IGraphBuilder::Connect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphBuilder.Connect
---

# IGraphBuilder::Connect


## -description

The <code>Connect</code> method connects the two pins, using intermediates if necessary.

## -parameters

### -param ppinOut [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface on the output pin.

### -param ppinIn [in]

Pointer to the <b>IPin</b> interface on the input pin.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_PARTIAL_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Partial success; some of the streams from this pin use an unsupported format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Operation aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
No combination of intermediate filters could be found to make the connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
At least one of the filters is not in the filter graph.

</td>
</tr>
</table>

## -remarks

This method connects two pins directly or indirectly, adding intermediate filters if necessary. The method starts by attempting a direct connection. If that fails, it tries to use any filters that are already in the filter graph and have unconnected input pins. (It enumerates these in an arbitrary order.) If that fails, it searches for filters in the registry, and tries them in order of merit. For more information, see <a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>.

During the connection process, the Filter Graph Manager ignores pins on intermediate filters if the pin name begins with a tilde (~). For more information, see [PIN_INFO](/windows/desktop/api/strmif/ns-strmif-pin_info).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>