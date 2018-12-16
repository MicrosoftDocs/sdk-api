---
UID: NF:shellscalingapi.RevokeScaleChangeNotifications
title: RevokeScaleChangeNotifications function
author: windows-sdk-content
description: Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.
old-location: shell\RevokeScaleChangeNotifications.htm
tech.root: shell
ms.assetid: 95F1D147-D364-4b11-AE2B-CD1FCEA07B5D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RevokeScaleChangeNotifications, RevokeScaleChangeNotifications function [Windows Shell], shell.RevokeScaleChangeNotifications, shellscalingapi/RevokeScaleChangeNotifications
ms.topic: function
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Shcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-0.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - RevokeScaleChangeNotifications
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RevokeScaleChangeNotifications function


## -description


Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="https://msdn.microsoft.com/4BF2F912-857A-4122-A9E1-6704F92240E6">UnregisterScaleChangeEvent</a> instead.</div><div> </div>

## -parameters




### -param displayDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh802761(v=VS.85).aspx">DISPLAY_DEVICE_TYPE</a></b>

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
 

 

