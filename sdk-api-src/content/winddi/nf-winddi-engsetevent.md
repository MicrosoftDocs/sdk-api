---
UID: NF:winddi.EngSetEvent
title: EngSetEvent function (winddi.h)
description: The EngSetEvent function sets the specified event object to the signaled state, and returns the event object's previous state.
helpviewer_keywords: ["EngSetEvent","EngSetEvent function [Display Devices]","display.engsetevent","gdifncs_1f6bd838-607b-47fa-bb1e-e21d92e65d39.xml","winddi/EngSetEvent"]
old-location: display\engsetevent.htm
tech.root: display
ms.assetid: 04e5d5e0-02b1-4335-9830-ecf04fdc0db1
ms.date: 12/05/2018
ms.keywords: EngSetEvent, EngSetEvent function [Display Devices], display.engsetevent, gdifncs_1f6bd838-607b-47fa-bb1e-e21d92e65d39.xml, winddi/EngSetEvent
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
 - EngSetEvent
 - winddi/EngSetEvent
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
 - EngSetEvent
---

# EngSetEvent function


## -description

The <b>EngSetEvent</b> function sets the specified event object to the signaled state, and returns the event object's previous state.

## -parameters

### -param pEvent [in]

Pointer to the event object that is to be set to the signaled state. This event object was returned by a previous call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.

## -returns

<b>EngSetEvent</b> returns a nonzero value if the event object's previous state was signaled.

## -remarks

Every event object is in either the signaled state or the nonsignaled state. Calling <b>EngSetEvent</b> causes the event object to be set to the signaled state.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwaitforsingleobject">EngWaitForSingleObject</a>