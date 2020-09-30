---
UID: NF:shobjidl.IAccessibilityDockingService.GetAvailableSize
title: IAccessibilityDockingService::GetAvailableSize (shobjidl.h)
description: Retrieves the dimensions available on a specific screen for displaying an accessibility window.
helpviewer_keywords: ["GetAvailableSize","GetAvailableSize method [Windows Shell]","GetAvailableSize method [Windows Shell]","IAccessibilityDockingService interface","IAccessibilityDockingService interface [Windows Shell]","GetAvailableSize method","IAccessibilityDockingService.GetAvailableSize","IAccessibilityDockingService::GetAvailableSize","shell.IAccessibilityDockingService_GetAvailableSize","shobjidl/IAccessibilityDockingService::GetAvailableSize"]
old-location: shell\IAccessibilityDockingService_GetAvailableSize.htm
tech.root: shell
ms.assetid: B447D464-EFAF-4743-900F-E77A2FE140DD
ms.date: 12/05/2018
ms.keywords: GetAvailableSize, GetAvailableSize method [Windows Shell], GetAvailableSize method [Windows Shell],IAccessibilityDockingService interface, IAccessibilityDockingService interface [Windows Shell],GetAvailableSize method, IAccessibilityDockingService.GetAvailableSize, IAccessibilityDockingService::GetAvailableSize, shell.IAccessibilityDockingService_GetAvailableSize, shobjidl/IAccessibilityDockingService::GetAvailableSize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibilityDockingService::GetAvailableSize
 - shobjidl/IAccessibilityDockingService::GetAvailableSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IAccessibilityDockingService.GetAvailableSize
---

# IAccessibilityDockingService::GetAvailableSize


## -description

Retrieves the dimensions available on a specific screen for displaying an accessibility window.

## -parameters

### -param hMonitor [in]

Type: <b>HMONITOR</b>

The handle of the monitor whose available docking size is to be retrieved. For information on how to retrieve an <b>HMONITOR</b>, see <a href="/windows/desktop/api/winuser/nf-winuser-monitorfromwindow">MonitorFromWindow</a>.

### -param pcxFixed [out]

Type: <b>UINT*</b>

When this method returns successfully, this parameter receives the fixed width, in physical pixels, available for docking on the specified monitor. Any window docked to this monitor will be sized to this width.

                        

If the method fails, this value is set to 0.

If this value is <b>NULL</b>, an access violation will occur.

### -param pcyMax [out]

Type: <b>UINT*</b>

When this method returns successfully, this parameter receives the maximum height, in physical pixels, available for a docked window on the specified monitor.

                        

If the method fails, this value is set to 0.

If this value is <b>NULL</b>, an access violation will occur.

## -returns

Type: <b>HRESULT</b>

Returns a standard return value, including the following:

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_MONITOR_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The monitor specified by <i>hMonitor</i> does not support docking.

</td>
</tr>
</table>

## -remarks

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
A docked accessibility window is limited in the amount of space that it can use on any screen. Therefore, before trying to dock an accessibility window, call this function to get the available dimensions. You cannot dock any window that would cause a Windows Store app to have access to less than 768 vertical screen pixels.


#### Examples

This example shows this method in use.


```

 IAccessibilityDockingService *pDockingService;
 
 HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
 if (SUCCEEDED(hr)) 
 {
     UINT uMaxHeight;
     UINT uFixedWidth;

     HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
     if (hMonitor != nullptr)
     {
         hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
     }
 }
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)">IAccessibilityDockingService</a>