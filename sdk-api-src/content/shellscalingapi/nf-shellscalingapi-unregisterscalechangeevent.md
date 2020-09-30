---
UID: NF:shellscalingapi.UnregisterScaleChangeEvent
title: UnregisterScaleChangeEvent function (shellscalingapi.h)
description: Unregisters for the scale change event registered through RegisterScaleChangeEvent. This function replaces RevokeScaleChangeNotifications.
helpviewer_keywords: ["UnregisterScaleChangeEvent","UnregisterScaleChangeEvent function [Windows Shell]","shell.UnregisterScaleChangeEvent","shellscalingapi/UnregisterScaleChangeEvent"]
old-location: shell\UnregisterScaleChangeEvent.htm
tech.root: shell
ms.assetid: 4BF2F912-857A-4122-A9E1-6704F92240E6
ms.date: 12/05/2018
ms.keywords: UnregisterScaleChangeEvent, UnregisterScaleChangeEvent function [Windows Shell], shell.UnregisterScaleChangeEvent, shellscalingapi/UnregisterScaleChangeEvent
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterScaleChangeEvent
 - shellscalingapi/UnregisterScaleChangeEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - UnregisterScaleChangeEvent
---

# UnregisterScaleChangeEvent function


## -description

Unregisters for the scale change event registered through <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>. This function replaces <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-revokescalechangenotifications">RevokeScaleChangeNotifications</a>.

## -parameters

### -param dwCookie [in]

A pointer to the cookie retrieved in the call to <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>