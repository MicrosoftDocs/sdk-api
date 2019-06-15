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
f1_keywords: ["mmc/IConsole2"]
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-expand">IConsole2::Expand</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-istaskpadviewpreferred">IConsole2::IsTaskpadViewPreferred</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-setstatustext">IConsole2::SetStatusText</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>. <b>IConsole2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-expand">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand or collapse an item in the scope pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814784(v=vs.85)">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-istaskpadviewpreferred">IsTaskpadViewPreferred</a>
</td>
<td align="left" width="63%">
Determines whether the user prefers taskpad views by default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814786(v=vs.85)">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814787(v=vs.85)">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814788(v=vs.85)">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Query for the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814789(v=vs.85)">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814790(v=vs.85)">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814791(v=vs.85)">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814792(v=vs.85)">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814793(v=vs.85)">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the header interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iconsole2-setstatustext">SetStatusText</a>
</td>
<td align="left" width="63%">
Enables the snap-in to change the text in the status bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814795(v=vs.85)">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa814796(v=vs.85)">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views because of content change.

</td>
</tr>
</table> 

