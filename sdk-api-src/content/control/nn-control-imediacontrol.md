---
UID: NN:control.IMediaControl
title: IMediaControl
author: windows-driver-content
description: The IMediaControl interface provides methods for controlling the flow of data through the filter graph.
old-location: dshow\imediacontrol.htm
old-project: DirectShow
ms.assetid: bce64088-3751-420c-b9de-b9b5f3119198
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMediaControl, IMediaControl interface [DirectShow], IMediaControl interface [DirectShow], described, IMediaControlInterface, control/IMediaControl, dshow.imediacontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaControl interface


## -description



The <code>IMediaControl</code> interface provides methods for controlling the flow of data through the filter graph. It includes methods for running, pausing, and stopping the graph. The Filter Graph Manager implements this interface. For more information on filter graph states, see <a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMediaControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b0d59a47-23a7-4e59-adfa-e01945a5d014">AddSourceFilter</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a14e971-365e-4061-8d07-01216e793864">get_FilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55257cef-2777-4a88-8805-e474e3b13c75">get_RegFilterCollection</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/653a94ff-6929-41b1-9b94-dccaff0f7ec7">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses all filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dfff776-da3f-40a3-86d4-76a5099d6e6f">RenderFile</a>
</td>
<td align="left" width="63%">
Intended for Visual Basic 6.0; not documented here.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Runs all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops all the filters in the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55dd55b1-51f0-4b47-8432-99741eaee8bb">StopWhenReady</a>
</td>
<td align="left" width="63%">
Pauses the filter graph, allowing filters to queue data, and then stops the filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

