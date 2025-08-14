---
UID: NF:winddi.EngUnmapEvent
title: EngUnmapEvent function (winddi.h)
description: The EngUnmapEvent function cleans up the kernel-mode resources allocated for a mapped user-mode event.
helpviewer_keywords: ["EngUnmapEvent","EngUnmapEvent function [Display Devices]","display.engunmapevent","gdifncs_0f5f2320-13d2-471a-93b6-739f9ecbd620.xml","winddi/EngUnmapEvent"]
old-location: display\engunmapevent.htm
tech.root: display
ms.assetid: 3be72e38-e7ea-407b-87e4-c6293d6160f6
ms.date: 12/05/2018
ms.keywords: EngUnmapEvent, EngUnmapEvent function [Display Devices], display.engunmapevent, gdifncs_0f5f2320-13d2-471a-93b6-739f9ecbd620.xml, winddi/EngUnmapEvent
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
 - EngUnmapEvent
 - winddi/EngUnmapEvent
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
 - EngUnmapEvent
---

# EngUnmapEvent function


## -description

The <b>EngUnmapEvent</b> function cleans up the kernel-mode resources allocated for a mapped user-mode event.

## -parameters

### -param pEvent [in]

Pointer to an event object returned from a previous call to <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.

## -returns

<b>EngUnmapEvent</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

## -remarks

The display driver should call <b>EngUnmapEvent</b> when it is notified that the process (typically <a href="/windows/desktop/api/winddi/nf-winddi-engcreatedriverobj">EngCreateDriverObj</a>) that created the user-mode event has terminated. The display driver can also call <b>EngUnmapEvent</b> to perform its own cleanup. The display and miniport drivers should not touch the event object after <b>EngUnmapEvent</b> has been called.

The display driver can call <b>EngUnmapEvent</b> only for an event object returned by <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>. It must not call this function for an event object returned by <a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatedriverobj">EngCreateDriverObj</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>