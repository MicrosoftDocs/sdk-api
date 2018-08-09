---
UID: NN:mmc.IConsoleNameSpace2
title: IConsoleNameSpace2
author: windows-sdk-content
description: The IConsoleNameSpace2 interface is introduced in MMC 1.1.
old-location: mmc\iconsolenamespace2.htm
old-project: MMC
ms.assetid: 894f99a6-2189-458d-a50f-497930d4a9dd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, IConsoleNameSpace2, IConsoleNameSpace2 interface [MMC], IConsoleNameSpace2 interface [MMC],described, _slate_iconsolenamespace2, mmc.iconsolenamespace2, mmc/IConsoleNameSpace, mmc/IConsoleNameSpace2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
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
 - IConsoleNameSpace2
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsoleNameSpace2 interface


## -description


The 
<b>IConsoleNameSpace2</b> interface is introduced in MMC 1.1.

The 
<b>IConsoleNameSpace2</b> interface enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer. For example, a snap-in that features a domain object might enumerate individual groups or organizations within the domain.

<b>IConsoleNameSpace2</b> supersedes the <b>IConsoleNameSpace</b> interface for MMC 1.1. In addition to inheriting all of the methods of <b>IConsoleNameSpace</b>, 
<b>IConsoleNameSpace2</b> has the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/3672babb-b172-4f25-8d95-61f3aacce2f0">IConsoleNameSpace2::Expand</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6057b8dd-d794-43a3-998b-689aafa28b9d">IConsoleNameSpace2::AddExtension</a>
</li>
</ul>The snap-in can query for a pointer to the 
<b>IConsoleNameSpace2</b> interface during a call to its 
<a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">IComponentData::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsoleNameSpace2</b> interface inherits from <b>IConsoleNameSpace</b>. <b>IConsoleNameSpace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsoleNameSpace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff537892">AddExtension</a>
</td>
<td align="left" width="63%">
Enables the snap-in to add a dynamic namespace extension to a selected item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/488a6c26-e064-44a1-9842-6f41ec25887c">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item from the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3672babb-b172-4f25-8d95-61f3aacce2f0">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand an item in the namespace without visibly expanding the item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a320f42e-1dca-4dd9-a919-c4451a48d105">GetChildItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the first child item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dadf9f0-4d49-49c3-a190-dfab0d6ace3f">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the attributes of a single scope pane item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d512370-bfe5-4a5a-b34b-c1096b6473a3">GetNextItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the next item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4534440-9fbe-41f1-bdf3-767c931a241b">GetParentItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the parent item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1966c4d1-acb1-496a-92d2-c0437c95fba6">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item into the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e63dd8dd-dcef-4d52-96f7-cf9a7e42a0f1">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the attributes of a single scope pane item.

</td>
</tr>
</table> 

