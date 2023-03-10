---
UID: NN:shobjidl_core.ITaskbarList3
title: ITaskbarList3 (shobjidl_core.h)
description: Extends ITaskbarList2 by exposing methods that support the unified launching and switching taskbar button functionality added in Windows 7.
helpviewer_keywords: ["ITaskbarList3","ITaskbarList3 interface [Windows Shell]","ITaskbarList3 interface [Windows Shell]","described","_shell_ITaskbarList3","shell.ITaskbarList3","shobjidl_core/ITaskbarList3"]
old-location: shell\ITaskbarList3.htm
tech.root: shell
ms.assetid: a5eb4e5a-df17-4aca-96fb-d8475e266b92
ms.date: 12/05/2018
ms.keywords: ITaskbarList3, ITaskbarList3 interface [Windows Shell], ITaskbarList3 interface [Windows Shell],described, _shell_ITaskbarList3, shell.ITaskbarList3, shobjidl_core/ITaskbarList3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList3
 - shobjidl_core/ITaskbarList3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3
---

# ITaskbarList3 interface


## -description

Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a> by exposing methods that support the unified launching and switching taskbar button functionality added in Windows 7. This functionality includes thumbnail representations and switch targets based on individual tabs in a tabbed application, thumbnail toolbars, notification and status overlays, and progress indicators.

## -inheritance

The <b>ITaskbarList3</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>. <b>ITaskbarList3</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a> interfaces, from which it inherits.

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
When an application displays a window, its taskbar button is created by the system. When the button is in place, the taskbar sends a <b>TaskbarButtonCreated</b> message to the window. Your application should call <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>(L"TaskbarButtonCreated") and handle that message in its wndproc. That message must be received by your application before it calls any <b>ITaskbarList3</b> method.

<div class="alert"><b>Note</b>  Applications cannot programmatically pin themselves to the taskbar. That functionality is reserved strictly for the user.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
