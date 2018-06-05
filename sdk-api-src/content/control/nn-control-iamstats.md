---
UID: NN:control.IAMStats
title: IAMStats
author: windows-sdk-content
description: The IAMStats interface retrieves performance data from the Filter Graph Manager.
old-location: dshow\iamstats.htm
old-project: DirectShow
ms.assetid: 01dbaba2-fdca-4f42-8816-fd99c4364dbd
ms.author: windowssdkdev
ms.date: 05/29/2018
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
tech.root: 
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
-	IAMStats
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMStats interface


## -description



The <code>IAMStats</code> interface retrieves performance data from the Filter Graph Manager. Filters can use this interface to record performance data.

<b>Filter developers</b>: As with all Filter Graph Manager interfaces, a filter must not hold a reference count on this interface, or it will cause a circular reference count. For more information, see <a href="https://msdn.microsoft.com/1f01c71f-5c12-4bf3-937c-740168baf776">IBaseFilter::JoinFilterGraph</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStats</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAMStats</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/a408b106-702c-4ecc-a424-b4b3588ea58f">AddValue</a>
</td>
<td align="left" width="63%">
Records a new value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48f2543a-7c93-4d4f-a568-b8066e9545fd">get_Count</a>
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
<a href="https://msdn.microsoft.com/c380deb0-bd49-4191-8218-d05aef39cb15">GetValueByName</a>
</td>
<td align="left" width="63%">
Retrieves a statistic by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
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
<th>
              Name
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>RenderFile</td>
<td>Measures the time taken by each call to <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>.</td>
</tr>
<tr>
<td>ConnectDirectInternal</td>
<td>Measures the time taken to connect two filters.</td>
</tr>
<tr>
<td>Build Mapper Cache</td>
<td>Measures the time taken to cache information about registered filters (used by the <a href="https://msdn.microsoft.com/cb8f25b3-a0f0-48fa-843f-88a5a5d17019">Filter Mapper</a> object).</td>
</tr>
<tr>
<td>Process Category <i>CategoryName</i></td>
<td>Measures the time taken to cache information about filters in a particular category, where <i>CategoryName</i> is the friendly name of the filter category. (See <a href="https://msdn.microsoft.com/cab4e2c9-eab9-4836-adfc-870490ca5b6b">Filter Categories</a>.)</td>
</tr>
</table>
 

For each of these statistics, the values represent time in milliseconds.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

