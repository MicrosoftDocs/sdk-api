---
UID: NF:shellscalingapi.RevokeScaleChangeNotifications
title: RevokeScaleChangeNotifications function (shellscalingapi.h)
description: Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.
helpviewer_keywords: ["RevokeScaleChangeNotifications","RevokeScaleChangeNotifications function [Windows Shell]","shell.RevokeScaleChangeNotifications","shellscalingapi/RevokeScaleChangeNotifications"]
old-location: shell\RevokeScaleChangeNotifications.htm
tech.root: shell
ms.assetid: 95F1D147-D364-4b11-AE2B-CD1FCEA07B5D
ms.date: 12/05/2018
ms.keywords: RevokeScaleChangeNotifications, RevokeScaleChangeNotifications function [Windows Shell], shell.RevokeScaleChangeNotifications, shellscalingapi/RevokeScaleChangeNotifications
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
req.lib: OneCore.Lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RevokeScaleChangeNotifications
 - shellscalingapi/RevokeScaleChangeNotifications
dev_langs:
 - c++
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
---

# RevokeScaleChangeNotifications function


## -description

Revokes the registration of a window, preventing it from receiving callbacks when scaling information changes.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a> instead.</div><div> </div>

## -parameters

### -param displayDevice [in]

Type: <b><a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-display_device_type">DISPLAY_DEVICE_TYPE</a></b>

The enum value that indicates which display device to receive notifications about.

### -param dwCookie [in]

Type: <b>DWORD</b>

The registration token returned by a previous call to <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangenotifications">RegisterScaleChangeNotifications</a>.

## -returns

Type: <b>STDAPI</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>