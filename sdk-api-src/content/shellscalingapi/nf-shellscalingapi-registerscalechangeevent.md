---
UID: NF:shellscalingapi.RegisterScaleChangeEvent
title: RegisterScaleChangeEvent function (shellscalingapi.h)
description: Registers for an event that is triggered when the scale has possibly changed. This function replaces RegisterScaleChangeNotifications.
helpviewer_keywords: ["RegisterScaleChangeEvent","RegisterScaleChangeEvent function [Windows Shell]","shell.RegisterScaleChangeEvent","shellscalingapi/RegisterScaleChangeEvent"]
old-location: shell\RegisterScaleChangeEvent.htm
tech.root: shell
ms.assetid: 05FAFC9B-DCB7-464A-9933-7166C7E53D40
ms.date: 12/05/2018
ms.keywords: RegisterScaleChangeEvent, RegisterScaleChangeEvent function [Windows Shell], shell.RegisterScaleChangeEvent, shellscalingapi/RegisterScaleChangeEvent
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
 - RegisterScaleChangeEvent
 - shellscalingapi/RegisterScaleChangeEvent
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
 - RegisterScaleChangeEvent
---

# RegisterScaleChangeEvent function


## -description

Registers for an event that is triggered when the scale has possibly changed. This function replaces <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangenotifications">RegisterScaleChangeNotifications</a>.

## -parameters

### -param hEvent [in]

Handle of the event to register for scale change notifications.

### -param pdwCookie [out]

When this function returns successfully, this value receives the address of a pointer to a cookie that can be used later to unregister for the scale change notifications through <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The event is raised whenever something that can affect scale changes, but just because the scale can be affected doesn't mean that it has been. Callers can cache the scale factor to verify that the monitor's scale actually has changed. The event handle will be duplicated, so callers can close their handle at any time.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>