---
UID: NF:dwmapi.DwmFlush
title: DwmFlush function (dwmapi.h)
description: Issues a flush call that blocks the caller until the next call to a Present method, when all of the Microsoft DirectX surface updates that are currently outstanding have been made. This compensates for very complex scenes or calling processes with very low priority.
helpviewer_keywords: ["DwmFlush","DwmFlush function [Desktop Window Manager]","_udwm_dwmflush","_udwm_dwmflush_cpp","dwm.dwmflush","dwmapi/DwmFlush","winui._udwm_dwmflush"]
old-location: dwm\dwmflush.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmflush.htm
ms.date: 12/05/2018
ms.keywords: DwmFlush, DwmFlush function [Desktop Window Manager], _udwm_dwmflush, _udwm_dwmflush_cpp, dwm.dwmflush, dwmapi/DwmFlush, winui._udwm_dwmflush
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmFlush
 - dwmapi/DwmFlush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
 - API-Ms-Win-DwmAPI-L1-1-0.dll
 - DComp.dll
api_name:
 - DwmFlush
---

## -description

Issues a flush call that blocks the caller until the next call to a Present method, when all of the Microsoft DirectX surface updates that are currently outstanding have been made. This compensates for very complex scenes or calling processes with very low priority.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>DwmFlush</b> waits for any queued DirectX changes that were queued by the calling application to be drawn to the screen before returning. It does not flush the entire session rendering batch.
