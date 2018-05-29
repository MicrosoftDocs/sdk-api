---
UID: NN:strmif.IFilterChain
title: IFilterChain
author: windows-sdk-content
description: The IFilterChain interface provides methods for starting, stopping, or removing chains of filters in a filter graph.
old-location: dshow\ifilterchain.htm
old-project: DirectShow
ms.assetid: 04fa1e89-19cd-488e-9df2-8a5fd2c3f445
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IFilterChain, IFilterChain interface [DirectShow], IFilterChain interface [DirectShow],described, IFilterChainInterface, dshow.ifilterchain, strmif/IFilterChain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFilterChain
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterChain interface


## -description



The <code>IFilterChain</code> interface provides methods for starting, stopping, or removing chains of filters in a filter graph. The filter graph manager exposes this interface.

A <i>filter chain</i> is a sequence of filters, each with at most one connected input pin and one connected output pin, that forms an unbroken line of filters. A filter chain is defined by the filter at the start of the chain and the filter at the end of the chain. (These can be the same filter, making a chain of one filter.) By definition, there is a single stream path going from the start of the chain downstream to the end of the chain.

The methods on this interface are useful in situations where an entire stream of data can appear or disappear, such as a video conferencing application that receives multiple streams over a network. For more information, see <a href="https://msdn.microsoft.com/13fed430-979b-40f7-91ba-aff2d811bd92">Dynamic Graph Building</a>. To control individual streams on a capture filter, use the <a href="https://msdn.microsoft.com/126c7ed7-acc0-4248-a3ab-c91c9f1c5cee">IAMStreamControl</a> interface instead.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterChain</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilterChain</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterChain</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a153ebf6-1d0a-45d0-ad2a-eb1eda62da2c">PauseChain</a>
</td>
<td align="left" width="63%">
Switches all the filters in a filter chain into a paused state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a47d2087-5f06-4fce-b573-16935370a34c">RemoveChain</a>
</td>
<td align="left" width="63%">
Removes every filter in a filter chain from the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095a8c28-d0f2-4c0d-9e96-eefd5786b88d">StartChain</a>
</td>
<td align="left" width="63%">
Switches all the filters in a filter chain into a running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03821fdb-8374-4386-868b-9bf7b2d83562">StopChain</a>
</td>
<td align="left" width="63%">
Switches all the filters in a filter chain into a stopped state.

</td>
</tr>
</table> 

