---
UID: NN:shobjidl_core.IFrameworkInputPane
title: IFrameworkInputPane (shobjidl_core.h)
description: Provides methods that enable apps to be informed of state changes and location for the input pane.
helpviewer_keywords: ["IFrameworkInputPane","IFrameworkInputPane interface [Windows Shell]","IFrameworkInputPane interface [Windows Shell]","described","shell.IFrameworkInputPane","shobjidl_core/IFrameworkInputPane"]
old-location: shell\IFrameworkInputPane.htm
tech.root: shell
ms.assetid: 05C115BA-249A-4271-9C6F-DAAEE91BB936
ms.date: 12/05/2018
ms.keywords: IFrameworkInputPane, IFrameworkInputPane interface [Windows Shell], IFrameworkInputPane interface [Windows Shell],described, shell.IFrameworkInputPane, shobjidl_core/IFrameworkInputPane
f1_keywords:
- shobjidl_core/IFrameworkInputPane
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFrameworkInputPane
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFrameworkInputPane interface


## -description


Provides methods that enable apps to be informed of state changes and location for the input pane. The input pane is a UI element, an on-screen keyboard or handwriting panel, that appears when the user performs an action that requires them to enter information, such as selecting a search box or an entry field in a form. Apps can then adjust their UI so that the input pane does not obscure items that the user might need to access while the input pane is shown.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFrameworkInputPane</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFrameworkInputPane</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFrameworkInputPane</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advise">Advise</a>
</td>
<td align="left" width="63%">
Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advisewithhwnd">AdviseWithHWND</a> in that it references its window through an object that implements <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icorewindow">ICoreWindow</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advisewithhwnd">AdviseWithHWND</a>
</td>
<td align="left" width="63%">
Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-advise">Advise</a> in that it references its window through an <b>HWND</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-location">Location</a>
</td>
<td align="left" width="63%">
Gets the current location of the input pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iframeworkinputpane-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters an app's input pane handler object so that it no longer receives notifications.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface; the implementation is supplied with Windows as CLSID_FrameworkInputPane.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

