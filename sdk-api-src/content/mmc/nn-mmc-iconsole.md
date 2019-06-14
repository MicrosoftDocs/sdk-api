---
UID: NN:mmc.IConsole
title: IConsole (mmc.h)
author: windows-sdk-content
description: Enables communication with the console.
old-location: mmc\iconsole.htm
tech.root: mmc
ms.assetid: 65154EB1-ABE5-4C4F-8B09-08633D82FD62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConsole, IConsole interface [MMC], IConsole interface [MMC],described, mmc.iconsole, mmc/IConsole
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
req.idl: Mmc.idl
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
 - IConsole
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConsole interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables communication with the console.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsole</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConsole</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsole</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-getmainwindow">GetMainWindow</a>
</td>
<td align="left" width="63%">
Returns a handle to the main frame window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>
</td>
<td align="left" width="63%">
Displays a message box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-newwindow">NewWindow</a>
</td>
<td align="left" width="63%">
Creates a new window rooted at the specified scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryconsoleverb">QueryConsoleVerb</a>
</td>
<td align="left" width="63%">
Query for the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryresultimagelist">QueryResultImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided result pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-queryresultview">QueryResultView</a>
</td>
<td align="left" width="63%">
Queries IConsole for the result view object's <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c21d454-2d3f-4e10-a4b0-135d20aea669">QueryScopeImageList</a>
</td>
<td align="left" width="63%">
Queries the console-provided scope pane's image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-selectscopeitem">SelectScopeItem</a>
</td>
<td align="left" width="63%">
Selects the given scope item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-setheader">SetHeader</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the header interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-settoolbar">SetToolbar</a>
</td>
<td align="left" width="63%">
Used by instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> only. Sets the toolbar interface to be used for this 
IComponent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-iconsole-updateallviews">UpdateAllViews</a>
</td>
<td align="left" width="63%">
Generates a notification to update views because of content change.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole3">IConsole3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
 

 

