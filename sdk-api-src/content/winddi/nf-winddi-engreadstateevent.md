---
UID: NF:winddi.EngReadStateEvent
title: EngReadStateEvent function (winddi.h)
description: The EngReadStateEvent function returns the current state of the specified event object:\_signaled or nonsignaled.
helpviewer_keywords: ["EngReadStateEvent","EngReadStateEvent function [Display Devices]","display.engreadstateevent","gdifncs_921fb236-706b-405c-affd-25811f97c7de.xml","winddi/EngReadStateEvent"]
old-location: display\engreadstateevent.htm
tech.root: display
ms.assetid: 32dddcc0-4cf2-467f-b1a6-03c9892d3473
ms.date: 12/05/2018
ms.keywords: EngReadStateEvent, EngReadStateEvent function [Display Devices], display.engreadstateevent, gdifncs_921fb236-706b-405c-affd-25811f97c7de.xml, winddi/EngReadStateEvent
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngReadStateEvent
 - winddi/EngReadStateEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngReadStateEvent
---

# EngReadStateEvent function


## -description

The <b>EngReadStateEvent</b> function returns the current state of the specified event object: signaled or nonsignaled.

## -parameters

### -param pEvent [in]

Pointer to the event object returned by a previous call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.

## -returns

<b>EngReadStateEvent</b> returns a nonzero value if the event object is currently set to the signaled state. If the event object is set to the nonsignaled state, this function returns zero.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>