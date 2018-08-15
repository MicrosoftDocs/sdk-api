---
UID: NN:mmc.IHeaderCtrl2
title: IHeaderCtrl2
author: windows-sdk-content
description: The IHeaderCtrl2 interface is introduced in MMC 1.2.
old-location: mmc\iheaderctrl2.htm
old-project: MMC
ms.assetid: fecf38be-6f45-45ea-a689-ff37b2b92922
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IHeaderCtrl2, IHeaderCtrl2 interface [MMC], IHeaderCtrl2 interface [MMC],described, _slate_iheaderctrl2, mmc.iheaderctrl2, mmc/IHeaderCtrl2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IHeaderCtrl2
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IHeaderCtrl2 interface


## -description


The 
<b>IHeaderCtrl2</b> interface is introduced in MMC 1.2.

The 
<b>IHeaderCtrl2</b> interface enables the manipulation of columns and indicates the kind of information that is to be presented in the result view pane of the console.

<b>IHeaderCtrl2</b> is a new version of the <b>IHeaderCtrl</b> interface for MMC 1.2. 
<b>IHeaderCtrl2</b> is the same as <b>IHeaderCtrl</b> with the addition of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/26a6a9bc-6556-4576-a810-d7c07c07cfd1">SetChangeTimeOut</a>
</li>
<li>
<a href="https://msdn.microsoft.com/df1257ee-66c4-4b63-a9c5-1bd0b94b4a85">SetColumnFilter</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2daf15ac-4de2-422d-9ac0-b592090468ed">GetColumnFilter</a>
</li>
</ul>These methods provide support for users to filter list views based on filters set on each column in the result view. Be aware that a return value of <b>E_NOTIMPL</b> by any one of these methods indicates that list view filtering is not available in the version of MMC in which the snap-in is loaded.

The 
<b>IHeaderCtrl2</b> interface can be queried from the 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole</a> interface passed into 
<a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">IComponent::Initialize</a> during the component's creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHeaderCtrl2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHeaderCtrl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHeaderCtrl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2739d0b9-6b34-4482-9a63-21029b39e04a">DeleteColumn</a>
</td>
<td align="left" width="63%">
Removes a column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2daf15ac-4de2-422d-9ac0-b592090468ed">GetColumnFilter</a>
</td>
<td align="left" width="63%">
Get filter data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cf09cc7-637d-4a60-90e8-b8904aa5c44b">GetColumnText</a>
</td>
<td align="left" width="63%">
Retrieves the text from a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07a7153a-23e6-46d3-84de-25cb44ef9300">GetColumnWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4de6dbf-6a2a-40fe-8f2f-c9a6f670f1a6">InsertColumn</a>
</td>
<td align="left" width="63%">
Adds a column to a default result view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26a6a9bc-6556-4576-a810-d7c07c07cfd1">SetChangeTimeOut</a>
</td>
<td align="left" width="63%">
Sets the time-out for filter change notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df1257ee-66c4-4b63-a9c5-1bd0b94b4a85">SetColumnFilter</a>
</td>
<td align="left" width="63%">
Set filter data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/274833c7-2bf4-401f-b211-5f5c97ead0c1">SetColumnText</a>
</td>
<td align="left" width="63%">
Sets the text in a specified column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3db2f03a-1dab-43ef-8922-727b5bb72843">SetColumnWidth</a>
</td>
<td align="left" width="63%">
Sets the width of a specified column.

</td>
</tr>
</table> 

