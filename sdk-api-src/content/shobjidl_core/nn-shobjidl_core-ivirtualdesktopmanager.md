---
UID: NN:shobjidl_core.IVirtualDesktopManager
title: IVirtualDesktopManager (shobjidl_core.h)
description: Exposes methods that enable an application to interact with groups of windows that form virtual workspaces.helpviewer_keywords: ["IVirtualDesktopManager","IVirtualDesktopManager interface [Windows Shell]","IVirtualDesktopManager interface [Windows Shell]","described","shell.ivirtualdesktopmanager","shobjidl_core/IVirtualDesktopManager"]
old-location: shell\ivirtualdesktopmanager.htm
tech.root: shell
ms.assetid: B95AC349-63E3-4A5A-A353-1C93486BB67A
ms.date: 12/05/2018
ms.keywords: IVirtualDesktopManager, IVirtualDesktopManager interface [Windows Shell], IVirtualDesktopManager interface [Windows Shell],described, shell.ivirtualdesktopmanager, shobjidl_core/IVirtualDesktopManager
f1_keywords:
- shobjidl_core/IVirtualDesktopManager
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IVirtualDesktopManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVirtualDesktopManager interface


## -description


Exposes methods that enable an application to interact with groups of windows that form virtual workspaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualDesktopManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVirtualDesktopManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVirtualDesktopManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ivirtualdesktopmanager-getwindowdesktopid">GetWindowDesktopId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the virtual desktop hosting the provided top-level window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ivirtualdesktopmanager-iswindowoncurrentvirtualdesktop">IsWindowOnCurrentVirtualDesktop</a>
</td>
<td align="left" width="63%">
Indicates whether the provided window is on the currently active virtual desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ivirtualdesktopmanager-movewindowtodesktop">MoveWindowToDesktop</a>
</td>
<td align="left" width="63%">
Moves a window to the specified virtual desktop.

</td>
</tr>
</table> 


## -remarks



The user can group a collection of windows together to create a virtual desktop. Every window is considered to be part of a virtual desktop. When one virtual desktop is hidden, all of the windows associated with it are also hidden. This enables the user to create multiple working environments and to be able to switch between them. Similarly, when a virtual desktop is selected to be active, the windows associated with that virtual desktop are displayed on the screen.

To support this concept, applications should avoid automatically switching the user from one virtual desktop to another. Only the user should instigate that change. In order to support this, newly created windows should appear on the currently active virtual desktop. In addition, if an application can reuse currently active windows, it should only reuse windows if they are on the currently active virtual desktop. Otherwise, a new window should be created.

<img alt="Virtual desktop visualization" src="./images/VirtualDesktops.png"/>
In the above image, the user has two virtual desktops and <b>VD2</b> is the currently active virtual desktop. If the user clicks a link in an outlook message, there's a URI activation that should open the link in an Internet Explorer window. If the user has configured IE to open links in the current window, it would normally use the currently open window. However, in this case, IE is on an inactive virtual desktop. In this scenario, IE should create a new window in the currently active virtual desktop.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/virtualdesktopmanager">VirtualDesktopManager</a>
 

 

