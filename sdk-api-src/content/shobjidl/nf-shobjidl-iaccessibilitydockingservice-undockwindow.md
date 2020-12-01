---
UID: NF:shobjidl.IAccessibilityDockingService.UndockWindow
title: IAccessibilityDockingService::UndockWindow (shobjidl.h)
description: Undocks the specified window handle if it is currently docked.
helpviewer_keywords: ["IAccessibilityDockingService interface [COM]","UndockWindow method","IAccessibilityDockingService.UndockWindow","IAccessibilityDockingService::UndockWindow","UndockWindow","UndockWindow method [COM]","UndockWindow method [COM]","IAccessibilityDockingService interface","com.iaccessibilitydockingservice_undockwindow","shobjidl/IAccessibilityDockingService::UndockWindow"]
old-location: com\iaccessibilitydockingservice_undockwindow.htm
tech.root: com
ms.assetid: 8A88D02C-E542-49F0-B423-771E755D506D
ms.date: 12/05/2018
ms.keywords: IAccessibilityDockingService interface [COM],UndockWindow method, IAccessibilityDockingService.UndockWindow, IAccessibilityDockingService::UndockWindow, UndockWindow, UndockWindow method [COM], UndockWindow method [COM],IAccessibilityDockingService interface, com.iaccessibilitydockingservice_undockwindow, shobjidl/IAccessibilityDockingService::UndockWindow
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibilityDockingService::UndockWindow
 - shobjidl/IAccessibilityDockingService::UndockWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl.h
api_name:
 - IAccessibilityDockingService.UndockWindow
---

# IAccessibilityDockingService::UndockWindow


## -description

Undocks the specified window handle if it is currently docked.

## -parameters

### -param hwnd

TBD

### -param hWnd [in]

Specifies the window that will be undocked.

## -returns

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The window does not belong to the calling process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_WINDOW_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The window is not docked.

</td>
</tr>
</table>

## -remarks

This method can only be used to undock windows that belong to the calling process.


#### Examples


```
class CAccessibilityApplicationWindow : public IAccessibilityDockingServiceCallback
{

    ....
    ....

    HRESULT _Undock()
    {
        return _pDockingService->UndockWindow(_hwndMyApplication);
    }

    IAccessibilityDockingService *_pDockingService;
    HWND _hwndMyApplication;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice">IAccessibilityDockingService</a>