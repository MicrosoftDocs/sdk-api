---
UID: NN:control.IMediaControl
title: IMediaControl (control.h)
description: The IMediaControl interface provides methods for controlling the flow of data through the filter graph.helpviewer_keywords: ["IMediaControl","IMediaControl interface [DirectShow]","IMediaControl interface [DirectShow]","described","IMediaControlInterface","control/IMediaControl","dshow.imediacontrol"]
old-location: dshow\imediacontrol.htm
tech.root: DirectShow
ms.assetid: bce64088-3751-420c-b9de-b9b5f3119198
ms.date: 12/05/2018
ms.keywords: IMediaControl, IMediaControl interface [DirectShow], IMediaControl interface [DirectShow],described, IMediaControlInterface, control/IMediaControl, dshow.imediacontrol
f1_keywords:
- control/IMediaControl
dev_langs:
- c++
req.header: control.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaControl interface


## -description



The <code>IMediaControl</code> interface provides methods for controlling the flow of data through the filter graph. It includes methods for running, pausing, and stopping the graph. The Filter Graph Manager implements this interface. For more information on filter graph states, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMediaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-addsourcefilter">AddSourceFilter</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-get_filtercollection">get_FilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-get_regfiltercollection">get_RegFilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses all filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-renderfile">RenderFile</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-run">Run</a>
</td>
<td align="left" width="63%">
Runs all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-stopwhenready">StopWhenReady</a>
</td>
<td align="left" width="63%">
Pauses the filter graph, allowing filters to queue data, and then stops the filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

