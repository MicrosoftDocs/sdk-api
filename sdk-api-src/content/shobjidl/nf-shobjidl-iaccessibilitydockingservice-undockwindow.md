---
UID: NF:shobjidl.IAccessibilityDockingService.UndockWindow
title: IAccessibilityDockingService::UndockWindow
author: windows-sdk-content
description: Undocks the specified window handle if it is currently docked.
old-location: com\iaccessibilitydockingservice_undockwindow.htm
old-project: com
ms.assetid: 8A88D02C-E542-49F0-B423-771E755D506D
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IAccessibilityDockingService interface [COM],UndockWindow method, IAccessibilityDockingService.UndockWindow, IAccessibilityDockingService::UndockWindow, UndockWindow, UndockWindow method [COM], UndockWindow method [COM],IAccessibilityDockingService interface, com.iaccessibilitydockingservice_undockwindow, shobjidl/IAccessibilityDockingService::UndockWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl.h
api_name:
 - IAccessibilityDockingService.UndockWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IAccessibilityDockingService::UndockWindow


## -description


Undocks the specified window handle if it is currently docked.


## -parameters




### -param hwnd






#### - hWnd [in]

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

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>class CAccessibilityApplicationWindow : public IAccessibilityDockingServiceCallback
{

    ....
    ....

    HRESULT _Undock()
    {
        return _pDockingService-&gt;UndockWindow(_hwndMyApplication);
    }

    IAccessibilityDockingService *_pDockingService;
    HWND _hwndMyApplication;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/DBAFE260-0AC6-4801-8590-DE058667C9A6">IAccessibilityDockingService</a>
 

 

