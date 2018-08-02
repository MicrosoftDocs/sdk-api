---
UID: NN:strmif.IDistributorNotify
title: IDistributorNotify
author: windows-sdk-content
description: The IDistributorNotify interface enables a plug-in distributor to be notified when the filter graph changes.Applications never use this interface.
old-location: dshow\idistributornotify.htm
old-project: DirectShow
ms.assetid: c7c9ee95-9d68-45c5-a3ca-8d6071782851
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDistributorNotify, IDistributorNotify interface [DirectShow], IDistributorNotify interface [DirectShow],described, IDistributorNotifyInterface, dshow.idistributornotify, strmif/IDistributorNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDistributorNotify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDistributorNotify interface


## -description



The <code>IDistributorNotify</code> interface enables a plug-in distributor to be notified when the filter graph changes.

Applications never use this interface. Implement this interface if you are writing a plug-in distributor (PID) and want the PID to receive notifications of control and changes in the composition of filter graphs.

The Filter Graph Manager queries for this interface on any plug-in distributors that it aggregates. If a PID exposes this interface, the Filter Graph Manager notifies the PID of any state changes by calling <b>IDistributorNotify</b> methods before calling the equivalent <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> methods on the filters. The Filter Graph Manager also calls the <a href="https://msdn.microsoft.com/5f77f674-643a-450a-9589-16866d6cf680">IDistributorNotify::NotifyGraphChange</a> method whenever it adds or removes a filter, or any pin connections change.

During a call to any <b>IDistributorNotify</b> method, do not hold any critical section that might be held by another code path that calls methods on the Filter Graph Manager. Doing so could result in a deadlock.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDistributorNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDistributorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDistributorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f77f674-643a-450a-9589-16866d6cf680">NotifyGraphChange</a>
</td>
<td align="left" width="63%">
Called when the set of filters in the filter graph change or their connections change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Called when the filter graph is entering a paused state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Called when the filter graph is entering a running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/671af56f-a333-441e-9a97-04226b1c3225">SetSyncSource</a>
</td>
<td align="left" width="63%">
Called when a new clock is registered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Called when the filter graph is entering a stopped state.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/80ff713d-f704-40d3-9317-cbf33d932207">Plug-in Distributors</a>
 

 

