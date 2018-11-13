---
UID: NF:shobjidl.IAccessibilityDockingService.DockWindow
title: IAccessibilityDockingService::DockWindow
author: windows-sdk-content
description: Docks an accessibility app window to the bottom of a screen while the system is in a full-screen or filled mode.
old-location: shell\IAccessibilityDockingService_DockWindow.htm
tech.root: shell
ms.assetid: D7B2AC62-D044-45b6-AF12-9BAC32A3B114
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DockWindow, DockWindow method [Windows Shell], DockWindow method [Windows Shell],IAccessibilityDockingService interface, IAccessibilityDockingService interface [Windows Shell],DockWindow method, IAccessibilityDockingService.DockWindow, IAccessibilityDockingService::DockWindow, shell.IAccessibilityDockingService_DockWindow, shobjidl/IAccessibilityDockingService::DockWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAccessibilityDockingService.DockWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibilityDockingService::DockWindow


## -description


Docks an accessibility app window to the bottom of a screen while the system is in a full-screen or filled mode.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the accessibility app window to dock on the monitor.


### -param hMonitor [in]

Type: <b>HMONITOR</b>

The monitor on which the accessibility app window will be docked.


### -param cyRequested [in]

Type: <b>UINT</b>

The requested height, in physical pixels, of the docked window. This must be less than or equal to the <i>pcyMax</i> value retrieved through <a href="https://msdn.microsoft.com/B447D464-EFAF-4743-900F-E77A2FE140DD">GetAvailableSize</a>).


### -param pCallback [in]

Type: <b><a href="https://msdn.microsoft.com/E357E47C-5A29-4b92-AD26-E604E501B7D6">IAccessibilityDockingServiceCallback</a>*</b>

A callback method pointer through which the accessibility app can receive a notification when the docked window is undocked.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The window handle or monitor handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process is not a UIAccess accessibility app or the calling process does not own the window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_DOCKOCCUPIED</b></dt>
</dl>
</td>
<td width="60%">
There is already another window occupying the docking space. Only one window can be docked at a time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMM_E_INSUFFICIENTHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The height requested in <i>cyRequested</i> is larger than the maximum allowed docking height for the specified monitor. Note that if this error code is returned, it means that this monitor supports docking, though for a window of less height. Call <a href="https://msdn.microsoft.com/B447D464-EFAF-4743-900F-E77A2FE140DD">GetAvailableSize</a> to determine the maximum value for <i>cyRequested</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_MONITOR_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The monitor specified by <i>hMonitor</i> does not support docking.

</td>
</tr>
</table>
 




## -remarks



This function will dock the specified window to the specified monitor. The window's new width will be the current width of the monitor. The window's new height will be <i>cyRequested</i> if it is less than the maximum available docking height for the monitor.


#### Examples

The following example shows the use of <b>DockWindow</b>. The method first calls <a href="https://msdn.microsoft.com/B447D464-EFAF-4743-900F-E77A2FE140DD">GetAvailableSize</a> to determine the maximum height of the docked window.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
 class CAccessibilityApplicationWindow : public IAccessibilityDockingServiceCallback
 {
     // ...
 
     HRESULT _Dock()
     {
         IAccessibilityDockingService *pDockingService;
        
         HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, 
                                       CLSCTX_INPROV_SERVER, 
                                       nullptr, 
                                       IID_PPV_ARGS(&amp;pDockingService));
         if (SUCCEEDED(hr)) 
         {
             UINT uMaxHeight;
             UINT uFixedWidth;
             
             HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
             if (hMonitor != nullptr)
             {
                 hr = pDockingService-&gt;GetAvailableSize(hMonitor, &amp;uMaxHeight, &amp;uFixedWidth);
                 if (SUCCEEDED(hr))
                 {
                     hr = pDockingService-&gt;DockWindow(_hwndMyApplication, hMonitor, uMaxHeight, this)
                 }
             }
         }
     }
 }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/EB66604E-4665-4d62-878C-7777C1C042F3">IAccessibilityDockingService</a>
 

 

