---
UID: NN:control.IMediaControl
title: IMediaControl
author: windows-sdk-content
description: The IMediaControl interface provides methods for controlling the flow of data through the filter graph.
old-location: dshow\imediacontrol.htm
old-project: DirectShow
ms.assetid: bce64088-3751-420c-b9de-b9b5f3119198
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMediaControl, IMediaControl interface [DirectShow], IMediaControl interface [DirectShow],described, IMediaControlInterface, control/IMediaControl, dshow.imediacontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: WMPContextMenuInfo
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaControl interface


## -description



The <code>IMediaControl</code> interface provides methods for controlling the flow of data through the filter graph. It includes methods for running, pausing, and stopping the graph. The Filter Graph Manager implements this interface. For more information on filter graph states, see <a href="https://msdn.microsoft.com/en-us/library/Dd388376(v=VS.85).aspx">Data Flow in the Filter Graph</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMediaControl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390171(v=VS.85).aspx">AddSourceFilter</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390173(v=VS.85).aspx">get_FilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390174(v=VS.85).aspx">get_RegFilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390172(v=VS.85).aspx">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390175(v=VS.85).aspx">Pause</a>
</td>
<td align="left" width="63%">
Pauses all filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390176(v=VS.85).aspx">RenderFile</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390177(v=VS.85).aspx">Run</a>
</td>
<td align="left" width="63%">
Runs all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390178(v=VS.85).aspx">Stop</a>
</td>
<td align="left" width="63%">
Stops all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390179(v=VS.85).aspx">StopWhenReady</a>
</td>
<td align="left" width="63%">
Pauses the filter graph, allowing filters to queue data, and then stops the filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

