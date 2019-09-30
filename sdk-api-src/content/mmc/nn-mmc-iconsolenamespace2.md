---
UID: NN:mmc.IConsoleNameSpace2
title: IConsoleNameSpace2 (mmc.h)
author: windows-sdk-content
description: The IConsoleNameSpace2 interface is introduced in MMC 1.1.
old-location: mmc\iconsolenamespace2.htm
tech.root: mmc
ms.assetid: 894f99a6-2189-458d-a50f-497930d4a9dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, IConsoleNameSpace2, IConsoleNameSpace2 interface [MMC], IConsoleNameSpace2 interface [MMC],described, _slate_iconsolenamespace2, mmc.iconsolenamespace2, mmc/IConsoleNameSpace, mmc/IConsoleNameSpace2
ms.topic: interface
f1_keywords: 
 - "mmc/IConsoleNameSpace2"
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleNameSpace2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-expand">IConsoleNameSpace2::Expand</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-addextension">IConsoleNameSpace2::AddExtension</a>
</li>
</ul>The snap-in can query for a pointer to the 
<b>IConsoleNameSpace2</b> interface during a call to its 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponentData::Initialize</a> method.


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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-addextension">AddExtension</a>
</td>
<td align="left" width="63%">
Enables the snap-in to add a dynamic namespace extension to a selected item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item from the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-expand">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand an item in the namespace without visibly expanding the item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getchilditem">GetChildItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the first child item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the attributes of a single scope pane item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getnextitem">GetNextItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the next item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-getparentitem">GetParentItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to get the handle to the parent item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-insertitem">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item into the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsolenamespace-setitem">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the attributes of a single scope pane item.

</td>
</tr>
</table> 

