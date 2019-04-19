---
UID: NN:mmc.IConsole2
title: IConsole2 (mmc.h)
author: windows-sdk-content
description: The IConsole2 interface is introduced in MMC 1.1.
old-location: mmc\iconsole2.htm
tech.root: mmc
ms.assetid: 9a20d09d-219c-4bcb-95b3-67a44e41629e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConsole2, IConsole2 interface [MMC], IConsole2 interface [MMC],described, _slate_iconsole2, mmc.iconsole2, mmc/IConsole2
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
 - IConsole2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsole2 interface


## -description


The 
<b>IConsole2</b> interface is introduced in MMC 1.1.

The 
<b>IConsole2</b> interface enables communication with the console.

<b>IConsole2</b> is the same as <b>IConsole</b> with the addition of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/958c9611-fd9c-4895-903b-145eacf76901">IConsole2::Expand</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c9221db-54d5-4dd2-8577-27915b313046">IConsole2::IsTaskpadViewPreferred</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31c95dcc-8bb8-4a11-9977-d4fa2ca30992">IConsole2::SetStatusText</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Mt300830(v=VS.85).aspx">IConsole</a>. <b>IConsole2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsole2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/958c9611-fd9c-4895-903b-145eacf76901">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand or collapse an item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0159545-0f39-4f3b-ace8-29ffb4ef638c">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c9221db-54d5-4dd2-8577-27915b313046">IsTaskpadViewPreferred</a>
</td>
<td align="left" width="63%">
Determines whether the user prefers taskpad views by default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cc90072-2766-43ec-8f3d-4bc1ca68325b">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0cbb4f-7374-4290-880d-ab81cb2ba3c0">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/439043b1-65a9-4208-94eb-e2aa1658ea81">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Query for the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaf91ea6-9389-4155-805c-72bbae99ca04">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26d4859c-e79f-4c63-92ad-b66de7d0fa13">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5cc356f-c8ea-4c4f-b643-3bfb6d7fb15b">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68e8473-a7ec-4e31-aef7-3e68c6a849c1">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bca6fbef-d00b-4f25-823e-fff76a96f59d">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the header interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31c95dcc-8bb8-4a11-9977-d4fa2ca30992">SetStatusText</a>
</td>
<td align="left" width="63%">
Enables the snap-in to change the text in the status bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a6d5ae-2541-4f64-8cc8-32ba2ae12605">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80ec84c1-111c-4605-9fa3-f5806fdc6fac">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views because of content change.

</td>
</tr>
</table> 

