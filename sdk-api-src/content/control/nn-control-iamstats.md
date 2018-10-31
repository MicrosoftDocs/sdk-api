---
UID: NN:control.IAMStats
title: IAMStats
author: windows-sdk-content
description: The IAMStats interface retrieves performance data from the Filter Graph Manager.
old-location: dshow\iamstats.htm
tech.root: DirectShow
ms.assetid: 01dbaba2-fdca-4f42-8816-fd99c4364dbd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAMStats, IAMStats interface [DirectShow], IAMStats interface [DirectShow],described, IAMStatsInterface, control/IAMStats, dshow.iamstats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: control.h
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
 - IAMStats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStats interface


## -description



The <code>IAMStats</code> interface retrieves performance data from the Filter Graph Manager. Filters can use this interface to record performance data.

<b>Filter developers</b>: As with all Filter Graph Manager interfaces, a filter must not hold a reference count on this interface, or it will cause a circular reference count. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd389529(v=VS.85).aspx">IBaseFilter::JoinFilterGraph</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStats</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAMStats</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IAMStats</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319778(v=VS.85).aspx">AddValue</a>
</td>
<td align="left" width="63%">
Records a new value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319782(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of statistics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ea650c-42dd-405c-8ad9-6e48cf51353d">GetIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index for a named statistic, or creates a new statistic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68a74f56-288b-4e7e-bb0d-a38d43e08c27">GetValueByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a statistic by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319781(v=VS.85).aspx">GetValueByName</a>
</td>
<td align="left" width="63%">
Retrieves a statistic by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319783(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets all statistics to zero.

</td>
</tr>
</table> 


## -remarks



Each statistic is defined by a name and an index. Use the <b>GetIndex</b> method to find the index from the name. Values are always <b>double</b> types. The following statistics are predefined.

<table>
<tr>
<th>Name
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>RenderFile</td>
<td>Measures the time taken by each call to <a href="https://msdn.microsoft.com/en-us/library/Dd390090(v=VS.85).aspx">IGraphBuilder::RenderFile</a>.</td>
</tr>
<tr>
<td>ConnectDirectInternal</td>
<td>Measures the time taken to connect two filters.</td>
</tr>
<tr>
<td>Build Mapper Cache</td>
<td>Measures the time taken to cache information about registered filters (used by the <a href="https://msdn.microsoft.com/en-us/library/Dd375788(v=VS.85).aspx">Filter Mapper</a> object).</td>
</tr>
<tr>
<td>Process Category <i>CategoryName</i></td>
<td>Measures the time taken to cache information about filters in a particular category, where <i>CategoryName</i> is the friendly name of the filter category. (See <a href="https://msdn.microsoft.com/en-us/library/Dd375655(v=VS.85).aspx">Filter Categories</a>.)</td>
</tr>
</table>
 

For each of these statistics, the values represent time in milliseconds.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

