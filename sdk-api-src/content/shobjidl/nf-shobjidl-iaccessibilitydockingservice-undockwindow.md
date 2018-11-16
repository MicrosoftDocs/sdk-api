---
UID: NF:shobjidl.IAccessibilityDockingService.UndockWindow
title: IAccessibilityDockingService::UndockWindow
author: windows-sdk-content
description: Undocks a currently docked accessibility app window from the bottom of the screen.
old-location: shell\IAccessibilityDockingService_UndockWindow.htm
tech.root: shell
ms.assetid: C3032B15-F5E1-48ef-919D-970603716F68
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAccessibilityDockingService interface [Windows Shell],UndockWindow method, IAccessibilityDockingService.UndockWindow, IAccessibilityDockingService::UndockWindow, UndockWindow, UndockWindow method [Windows Shell], UndockWindow method [Windows Shell],IAccessibilityDockingService interface, shell.IAccessibilityDockingService_UndockWindow, shobjidl/IAccessibilityDockingService::UndockWindow
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
 - IAccessibilityDockingService.UndockWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl.h
: 
- IAccessibilityDockingService.UndockWindow
: 
---

# IAccessibilityDockingService::UndockWindow


## -description


Undocks a currently docked accessibility app window from the bottom of the screen.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window to undock.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The specified window does not belong to the calling process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_WINDOW_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The specified window is not docked.

</td>
</tr>
</table>
 




## -remarks



This method can only be used to undock windows that belong to the calling process.


#### Examples

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>


class CAccessibilityApplicationWindow : public IAccessibilityDockingServiceCallback
{

    ....
    ....

    HRESULT _Undock()
    {
        return _pDockingService-&gt;UndockWindow(_hwndMyApplication);
    }

    IAccessibilityDockingService *_pDockingService;
    HWND _hwndMyApplication;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/EB66604E-4665-4d62-878C-7777C1C042F3">IAccessibilityDockingService</a>
 

 

