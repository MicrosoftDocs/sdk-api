---
UID: NN:shobjidl.IAccessibilityDockingService
title: IAccessibilityDockingService
author: windows-sdk-content
description: Docks a single accessibility app window to the bottom of a screen.
old-location: shell\IAccessibilityDockingService.htm
tech.root: shell
ms.assetid: EB66604E-4665-4d62-878C-7777C1C042F3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAccessibilityDockingService, IAccessibilityDockingService interface [Windows Shell], IAccessibilityDockingService interface [Windows Shell],described, shell.IAccessibilityDockingService, shobjidl/IAccessibilityDockingService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IAccessibilityDockingService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibilityDockingService interface


## -description


Docks a single accessibility app window to the bottom of a screen.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibilityDockingService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibilityDockingService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibilityDockingService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D7B2AC62-D044-45b6-AF12-9BAC32A3B114">DockWindow</a>
</td>
<td align="left" width="63%">
Docks an accessibility app window to the bottom of a screen while the system is in a full-screen or filled mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B447D464-EFAF-4743-900F-E77A2FE140DD">GetAvailableSize</a>
</td>
<td align="left" width="63%">
Retrieves the dimensions available on a specific screen for displaying an accessibility window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C3032B15-F5E1-48ef-919D-970603716F68">UndockWindow</a>
</td>
<td align="left" width="63%">
Undocks a currently docked accessibility app window from the bottom of the screen.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
A default implementation of this interface is provided with Windows. Do not implement your own version. The default implementation can be cocreated using CLSID_AccessibilityDockingService.

<h3><a id="Purpose"></a><a id="purpose"></a><a id="PURPOSE"></a>Purpose</h3>
Windows users want to be able to use non-transient UI accessibility tools such as on-screen keyboards while using their Windows Store apps, without those accessibility UI elements blocking the view of the app. <b>IAccessibilityDockingService</b> enables an accessibility app to dock a single accessibility window to the bottom of the screen. In the case of multiple monitors, the window is docked to the bottom of the screen on the monitor that displays the Start screen. When the app docks its accessibility window, existing apps resize so that the accessibility window does not cover anything in the new Windows UI. From the user's point of view, the accessibility window becomes part of the new Windows UI.

Accessibility app developers can use this interface to dock their application window in one of two situations:
                    
                        <ul>
<li>A Windows Store app is visible and not snapped.</li>
<li>The Launcher is visible.</li>
</ul>


<h3><a id="Threading"></a><a id="threading"></a><a id="THREADING"></a>Threading</h3>
This object is apartment-threaded. It will not have an impact on the calling thread's COM apartment and is safe to call on a UI thread. However, because <b>IAccessibilityDockingService</b> synchronously positions the window when it is being docked, it is important that the UI thread that belongs to that window is not blocked when <a href="https://msdn.microsoft.com/D7B2AC62-D044-45b6-AF12-9BAC32A3B114">IAccessibilityDockingService::DockWindow</a> is called.

<b>IAccessibilityDockingService</b> works with the <a href="https://msdn.microsoft.com/AFD60F5B-3017-49a2-8AFC-8309D11B3ACA">IAccessibilityDockingServiceCallback::Undocked</a> method. Callback listeners receive this notification when they have been forcibly undocked. The callback occurs in the same COM apartment in which the call to <a href="https://msdn.microsoft.com/D7B2AC62-D044-45b6-AF12-9BAC32A3B114">IAccessibilityDockingService::DockWindow</a> was made.

<h3><a id="Usage_notes"></a><a id="usage_notes"></a><a id="USAGE_NOTES"></a>Usage notes</h3>
When your app's window is docked, you must ensure that you have the WS_EX_TOOLWINDOW style set on your window. Otherwise, it will end up being moved out of position after <a href="https://msdn.microsoft.com/D7B2AC62-D044-45b6-AF12-9BAC32A3B114">DockWindow</a> is called. The following code demonstrates how to do this. Please see MSDN for information on these flags and their interaction with 
<a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a> and <a href="https://msdn.microsoft.com/6c7c4f93-8b6b-403d-a8c7-954d69b37b59">SetWindowLongPtr</a>.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
 // Set the window style
 LONG_PTR OldWindowExStyle = GetWindowLongPtr(hwnd, GWL_EXSTYLE);
 LONG_PTR NewWindowExStyle = OldWindowExStyle | WS_EX_TOOLWINDOW;
 SetWindowLongPtr(hwnd, GWL_EXSTYLE, NewWindowExStyle);

 // In order to make the new window style take effect, we call SetWindowPos.
 SetWindowPos(hwnd, NULL, 0, 0, 0, 0, SWP_NOMOVE | SWP_NOSIZE | SWP_NOZORDER | SWP_FRAMECHANGED | SWP_NOACTIVATE);</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Security"></a><a id="security"></a><a id="SECURITY"></a>Security</h3>
Use of this API requires a callback interface pointer (<a href="https://msdn.microsoft.com/E357E47C-5A29-4b92-AD26-E604E501B7D6">IAccessibilityDockingServiceCallback</a>) to be passed from a higher integrity-level process (the accessibility app) to a lower integrity-level process (the Shell). Accessibility app developers should be aware that a lower integrity-level process will call <a href="https://msdn.microsoft.com/AFD60F5B-3017-49a2-8AFC-8309D11B3ACA">IAccessibilityDockingServiceCallback::Undocked</a>. The data passed to the accessibility app is an enumeration value.



