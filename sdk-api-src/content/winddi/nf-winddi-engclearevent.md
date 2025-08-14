---
UID: NF:winddi.EngClearEvent
title: EngClearEvent function (winddi.h)
description: The EngClearEvent function sets a specified event object to the nonsignaled state.
helpviewer_keywords: ["EngClearEvent","EngClearEvent function [Display Devices]","display.engclearevent","gdifncs_0650b2ea-0f64-425b-bfd4-a7c369f2915b.xml","winddi/EngClearEvent"]
old-location: display\engclearevent.htm
tech.root: display
ms.assetid: fa87ed4f-4ccb-465c-bcd5-890694b790a3
ms.date: 12/05/2018
ms.keywords: EngClearEvent, EngClearEvent function [Display Devices], display.engclearevent, gdifncs_0650b2ea-0f64-425b-bfd4-a7c369f2915b.xml, winddi/EngClearEvent
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
 - EngClearEvent
 - winddi/EngClearEvent
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
 - EngClearEvent
---

# EngClearEvent function


## -description

The <b>EngClearEvent</b> function sets a specified event object to the nonsignaled state.

## -parameters

### -param pEvent [in]

Pointer to the event object returned by a previous call to either <a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>