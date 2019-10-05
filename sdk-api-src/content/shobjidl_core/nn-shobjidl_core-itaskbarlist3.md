---
UID: NN:shobjidl_core.ITaskbarList3
title: ITaskbarList3 (shobjidl_core.h)
author: windows-sdk-content
description: Extends ITaskbarList2 by exposing methods that support the unified launching and switching taskbar button functionality added in Windows 7.
old-location: shell\ITaskbarList3.htm
tech.root: shell
ms.assetid: a5eb4e5a-df17-4aca-96fb-d8475e266b92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskbarList3, ITaskbarList3 interface [Windows Shell], ITaskbarList3 interface [Windows Shell],described, _shell_ITaskbarList3, shell.ITaskbarList3, shobjidl_core/ITaskbarList3
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/ITaskbarList3"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskbarList3 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a> by exposing methods that support the unified launching and switching taskbar button functionality added in Windows 7. This functionality includes thumbnail representations and switch targets based on individual tabs in a tabbed application, thumbnail toolbars, notification and status overlays, and progress indicators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskbarList3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>. <b>ITaskbarList3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskbarList3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab">RegisterTab</a>
</td>
<td align="left" width="63%">
Informs the taskbar that a new tab or document thumbnail has been provided for display in an application's taskbar group flyout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon">SetOverlayIcon</a>
</td>
<td align="left" width="63%">
Applies an overlay to a taskbar button to indicate application status or a notification to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate">SetProgressState</a>
</td>
<td align="left" width="63%">
Sets the type and state of the progress indicator displayed on a taskbar button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue">SetProgressValue</a>
</td>
<td align="left" width="63%">
Displays or updates a progress bar hosted in a taskbar button to show the specific percentage completed of the full operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive">SetTabActive</a>
</td>
<td align="left" width="63%">
Informs the taskbar that a tab or document window has been made the active window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder">SetTabOrder</a>
</td>
<td align="left" width="63%">
Inserts a new thumbnail into a TDI or MDI application's group flyout or moves an existing thumbnail to a new position in the application's group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip">SetThumbnailClip</a>
</td>
<td align="left" width="63%">
Selects a portion of a window's client area to display as that window's thumbnail in the taskbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailtooltip">SetThumbnailTooltip</a>
</td>
<td align="left" width="63%">
Specifies or updates the text of the tooltip that is displayed when the mouse pointer rests on an individual preview thumbnail in a taskbar button flyout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons">ThumbBarAddButtons</a>
</td>
<td align="left" width="63%">
Adds a thumbnail toolbar with a specified set of buttons to the thumbnail image of a window in a taskbar button flyout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist">ThumbBarSetImageList</a>
</td>
<td align="left" width="63%">
Specifies an image list that contains button images for a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ThumbBarUpdateButtons</a>
</td>
<td align="left" width="63%">
Shows, enables, disables, or hides buttons in a thumbnail toolbar as required by the window's current state. A thumbnail toolbar is a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab">UnregisterTab</a>
</td>
<td align="left" width="63%">
Removes a thumbnail from an application's preview group when that tab or document is closed in the application.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_TaskbarList. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the methods of this interface to do the following:

<ul>
<li>When working with a TDI application (such as Windows Internet Explorer) or a MDI application (such as Microsoft Excel) that is displaying its windows as a group on the taskbar:
                        
                        <ul>
<li>Provide the taskbar with a thumbnail that represents the view of an individual tab or document.</li>
<li>Remove the thumbnail of an individual tab or document from the group.</li>
<li>Change the order of thumbnails in the group.</li>
<li>Set a tab thumbnail as the selected item when the thumbnails are shown.</li>
</ul>
</li>
<li>When applying an overlay to a taskbar icon, such as a notification.</li>
<li>When showing the progress of an operation, such as copying or installing an item.</li>
<li>When adding a toolbar to a thumbnail.</li>
</ul>
When an application displays a window, its taskbar button is created by the system. When the button is in place, the taskbar sends a <b>TaskbarButtonCreated</b> message to the window. Your application should call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>(L"TaskbarButtonCreated") and handle that message in its wndproc. That message must be received by your application before it calls any <b>ITaskbarList3</b> method.

<div class="alert"><b>Note</b>  Applications cannot programmatically pin themselves to the taskbar. That functionality is reserved strictly for the user.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
 

 

