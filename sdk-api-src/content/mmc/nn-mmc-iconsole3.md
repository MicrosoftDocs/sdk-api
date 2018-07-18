---
UID: NN:mmc.IConsole3
title: IConsole3
author: windows-sdk-content
description: The IConsole3 interface supersedes the IConsole2 interface. The IConsole3 interface contains the IConsole3::RenameScopeItem method, which allows a scope node to programmatically be placed in rename mode.
old-location: mmc\iconsole3.htm
old-project: MMC
ms.assetid: be3d42a4-a18a-40a5-99fc-2cf2a848c564
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IConsole3, IConsole3 interface [MMC], IConsole3 interface [MMC],described, _slate_iconsole3, mmc.iconsole3, mmc/IConsole3
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
 - IConsole3
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole3 interface


## -description


The 
<b>IConsole3</b> interface supersedes the 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a> interface. The 
<b>IConsole3</b> interface contains the 
<a href="https://msdn.microsoft.com/ebbdc395-e94f-4e86-965c-59bf7a49bbeb">IConsole3::RenameScopeItem</a> method, which allows a scope node to programmatically be placed in rename mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConsole3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsole3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/958c9611-fd9c-4895-903b-145eacf76901">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand or collapse an item in the scope pane.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0159545-0f39-4f3b-ace8-29ffb4ef638c">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c9221db-54d5-4dd2-8577-27915b313046">IsTaskpadViewPreferred</a>
</td>
<td align="left" width="63%">
Determines if the user prefers taskpad views by default.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cc90072-2766-43ec-8f3d-4bc1ca68325b">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0cbb4f-7374-4290-880d-ab81cb2ba3c0">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/439043b1-65a9-4208-94eb-e2aa1658ea81">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Queries for the 
<a href="https://msdn.microsoft.com/9c4338c1-eb5e-47f3-8b5b-0623690bd5f6">IConsoleVerb</a> interface.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaf91ea6-9389-4155-805c-72bbae99ca04">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26d4859c-e79f-4c63-92ad-b66de7d0fa13">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5cc356f-c8ea-4c4f-b643-3bfb6d7fb15b">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebbdc395-e94f-4e86-965c-59bf7a49bbeb">RenameScopeItem</a>
</td>
<td align="left" width="63%">
Allows a specified scope node to programmatically be placed in rename mode.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68e8473-a7ec-4e31-aef7-3e68c6a849c1">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bca6fbef-d00b-4f25-823e-fff76a96f59d">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the header interface to be used for this 
IComponent interface.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31c95dcc-8bb8-4a11-9977-d4fa2ca30992">SetStatusText</a>
</td>
<td align="left" width="63%">
Enables the snap-in to change the text on the status bar.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a6d5ae-2541-4f64-8cc8-32ba2ae12605">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent interface.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80ec84c1-111c-4605-9fa3-f5806fdc6fac">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views when the content changes.</p> (Inherited from <a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>)</td>
</tr>
</table> 

