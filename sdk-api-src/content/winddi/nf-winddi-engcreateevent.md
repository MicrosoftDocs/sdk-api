---
UID: NF:winddi.EngCreateEvent
title: EngCreateEvent function (winddi.h)
description: The EngCreateEvent function creates a synchronization event object that can be used to synchronize hardware access between a display driver and the video miniport driver.
helpviewer_keywords: ["EngCreateEvent","EngCreateEvent function [Display Devices]","display.engcreateevent","gdifncs_d8f6efc2-d0a2-4790-88c5-16e4487e2ce2.xml","winddi/EngCreateEvent"]
old-location: display\engcreateevent.htm
tech.root: display
ms.assetid: 0fe4c840-ba85-492c-ac3d-b7c8639d1210
ms.date: 12/05/2018
ms.keywords: EngCreateEvent, EngCreateEvent function [Display Devices], display.engcreateevent, gdifncs_d8f6efc2-d0a2-4790-88c5-16e4487e2ce2.xml, winddi/EngCreateEvent
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
 - EngCreateEvent
 - winddi/EngCreateEvent
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
 - EngCreateEvent
---

# EngCreateEvent function


## -description

The <b>EngCreateEvent</b> function creates a synchronization event object that can be used to synchronize hardware access between a display driver and the video miniport driver.

## -parameters

### -param ppEvent [out]

Pointer to a location in which a valid event object is returned.

## -returns

<b>EngCreateEvent</b> returns <b>TRUE</b> if it is successful in creating an event object. Otherwise, it returns <b>FALSE</b>.

## -remarks

<b>EngCreateEvent</b> creates a synchronization event object, which is initialized to the nonsignaled state.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engdeleteevent">EngDeleteEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engsetevent">EngSetEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwaitforsingleobject">EngWaitForSingleObject</a>