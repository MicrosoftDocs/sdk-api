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

# RevokeScaleChangeNotifications function


## -description


Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a> instead.</div><div> </div>

## -parameters




### -param displayDevice [in]

Type: <b><a href="https://msdn.microsoft.com/C8964494-339B-4198-A544-3BBCCFEB9596">DISPLAY_DEVICE_TYPE</a></b>

The enum value that indicates which display device to receive notifications about.


### -param dwCookie [in]

Type: <b>DWORD</b>

The registration token returned by a previous call to <a href="https://msdn.microsoft.com/79FB0A54-EBF0-4aab-B631-B4D3EA54D20B">RegisterScaleChangeNotifications</a>.


## -returns



Type: <b>STDAPI</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2F214512-704D-41A2-86A6-1EF880CD3DB4">GetScaleFactorForMonitor</a>



<a href="https://msdn.microsoft.com/05FAFC9B-DCB7-464A-9933-7166C7E53D40">RegisterScaleChangeEvent</a>



<a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a>
 

 

