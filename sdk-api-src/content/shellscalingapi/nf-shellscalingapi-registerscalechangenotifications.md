---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# RegisterScaleChangeNotifications function


## -description


Registers a window to receive callbacks when scaling information changes.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a> instead.</div><div> </div>

## -parameters




### -param displayDevice [in]

Type: <b><a href="https://msdn.microsoft.com/C8964494-339B-4198-A544-3BBCCFEB9596">DISPLAY_DEVICE_TYPE</a></b>

The enum value that indicates which display device to receive notifications about.


### -param hwndNotify [in]

Type: <b>HWND</b>

The handle of the window that will receive the notifications.


### -param uMsgNotify [in]

Type: <b>UINT</b>

An application-defined message that is passed to the window specified by <i>hwndNotify</i> when scaling information changes.  Typically, this should be set to <a href="https://msdn.microsoft.com/fdb549df-426f-4af5-9c17-6e8730e4abc0">WM_APP</a>+<i>x</i>, where <i>x</i> is an integer value.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

Pointer to a value that, when this function returns successfully, receives a registration token. This token is used to revoke notifications by calling <a href="https://msdn.microsoft.com/95F1D147-D364-4b11-AE2B-CD1FCEA07B5D">RevokeScaleChangeNotifications</a>.


## -returns



Type: <b>STDAPI</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This message specified by <i>uMsgNotify</i> is posted to the registered window through <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>. The <i>wParam</i> of the message can contain a combination of <a href="https://msdn.microsoft.com/18B3E8F1-C9A9-4CE4-8982-C552486EA9B1">SCALE_CHANGE_FLAGS</a> that describe  the change that occurred.




## -see-also




<a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a>



<a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>



<a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>
 

 

