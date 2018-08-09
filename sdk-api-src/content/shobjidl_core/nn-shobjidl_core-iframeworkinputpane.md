---
UID: NN:shobjidl_core.IFrameworkInputPane
title: IFrameworkInputPane
author: windows-sdk-content
description: Provides methods that enable apps to be informed of state changes and location for the input pane.
old-location: shell\IFrameworkInputPane.htm
old-project: shell
ms.assetid: 05C115BA-249A-4271-9C6F-DAAEE91BB936
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFrameworkInputPane, IFrameworkInputPane interface [Windows Shell], IFrameworkInputPane interface [Windows Shell],described, shell.IFrameworkInputPane, shobjidl_core/IFrameworkInputPane
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFrameworkInputPane
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IFrameworkInputPane interface


## -description


Provides methods that enable apps to be informed of state changes and location for the input pane. The input pane is a UI element, an on-screen keyboard or handwriting panel, that appears when the user performs an action that requires them to enter information, such as selecting a search box or an entry field in a form. Apps can then adjust their UI so that the input pane does not obscure items that the user might need to access while the input pane is shown.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFrameworkInputPane</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFrameworkInputPane</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F05A097F-13A4-48ad-B660-5B2409BB6D61">Advise</a>
</td>
<td align="left" width="63%">
Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://msdn.microsoft.com/6C4F52DC-0ED0-4A2D-9C5F-F29063E1AAEE">AdviseWithHWND</a> in that it references its window through an object that implements <a href="https://msdn.microsoft.com/34222b7d-b501-4d5e-8e6e-f1cb8fbdbfc9">ICoreWindow</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C4F52DC-0ED0-4A2D-9C5F-F29063E1AAEE">AdviseWithHWND</a>
</td>
<td align="left" width="63%">
Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://msdn.microsoft.com/F05A097F-13A4-48ad-B660-5B2409BB6D61">Advise</a> in that it references its window through an <b>HWND</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556493">Location</a>
</td>
<td align="left" width="63%">
Gets the current location of the input pane.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943">Unadvise</a>
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




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

