---
UID: NF:winddi.EngClearEvent
title: EngClearEvent function (winddi.h)

description: The EngClearEvent function sets a specified event object to the nonsignaled state.
old-location: display\engclearevent.htm
tech.root: display
ms.assetid: fa87ed4f-4ccb-465c-bcd5-890694b790a3

ms.date: 12/05/2018
ms.keywords: EngClearEvent, EngClearEvent function [Display Devices], display.engclearevent, gdifncs_0650b2ea-0f64-425b-bfd4-a7c369f2915b.xml, winddi/EngClearEvent
ms.topic: function
f1_keywords: 
 - "winddi/EngClearEvent"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngClearEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngClearEvent function


## -description


The <b>EngClearEvent</b> function sets a specified event object to the nonsignaled state.


## -parameters




### -param pEvent [in]

Pointer to the event object returned by a previous call to either <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.


## -returns



None




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>
 

 

