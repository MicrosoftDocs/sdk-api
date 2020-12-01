---
UID: NN:mmc.IConsole3
title: IConsole3 (mmc.h)
description: The IConsole3 interface supersedes the IConsole2 interface. The IConsole3 interface contains the IConsole3::RenameScopeItem method, which allows a scope node to programmatically be placed in rename mode.
helpviewer_keywords: ["IConsole3","IConsole3 interface [MMC]","IConsole3 interface [MMC]","described","_slate_iconsole3","mmc.iconsole3","mmc/IConsole3"]
old-location: mmc\iconsole3.htm
tech.root: mmc
ms.assetid: be3d42a4-a18a-40a5-99fc-2cf2a848c564
ms.date: 12/05/2018
ms.keywords: IConsole3, IConsole3 interface [MMC], IConsole3 interface [MMC],described, _slate_iconsole3, mmc.iconsole3, mmc/IConsole3
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
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsole3
 - mmc/IConsole3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole3
---

# IConsole3 interface


## -description

The 
<b>IConsole3</b> interface supersedes the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> interface. The 
<b>IConsole3</b> interface contains the 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole3-renamescopeitem">IConsole3::RenameScopeItem</a> method, which allows a scope node to programmatically be placed in rename mode.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole3</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConsole3</b> also has these types of members:
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
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-expand">Expand</a>
</td>
<td align="left" width="63%">
Enables the snap-in to expand or collapse an item in the scope pane.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814784(v=vs.85)">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-istaskpadviewpreferred">IsTaskpadViewPreferred</a>
</td>
<td align="left" width="63%">
Determines if the user prefers taskpad views by default.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814786(v=vs.85)">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814787(v=vs.85)">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814788(v=vs.85)">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Queries for the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a> interface.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814789(v=vs.85)">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814790(v=vs.85)">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814791(v=vs.85)">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole3-renamescopeitem">RenameScopeItem</a>
</td>
<td align="left" width="63%">
Allows a specified scope node to programmatically be placed in rename mode.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814792(v=vs.85)">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814793(v=vs.85)">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the header interface to be used for this 
IComponent interface.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-setstatustext">SetStatusText</a>
</td>
<td align="left" width="63%">
Enables the snap-in to change the text on the status bar.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814795(v=vs.85)">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent interface.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa814796(v=vs.85)">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views when the content changes.</p> (Inherited from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>)</td>
</tr>
</table>