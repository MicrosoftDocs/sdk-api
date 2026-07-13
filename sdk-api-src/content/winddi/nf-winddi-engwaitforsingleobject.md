---
UID: NF:winddi.EngWaitForSingleObject
title: EngWaitForSingleObject function (winddi.h)
description: The EngWaitForSingleObject function puts the current thread of the display driver into a wait state until the specified event object is set to the signaled state, or until the wait times out.
helpviewer_keywords: ["EngWaitForSingleObject","EngWaitForSingleObject function [Display Devices]","display.engwaitforsingleobject","gdifncs_12c16d6b-ff3f-4cd4-8d4c-150ab8377dfb.xml","winddi/EngWaitForSingleObject"]
old-location: display\engwaitforsingleobject.htm
tech.root: display
ms.assetid: a2a1c7ad-1e56-45f7-83de-49ebc0d831f9
ms.date: 12/05/2018
ms.keywords: EngWaitForSingleObject, EngWaitForSingleObject function [Display Devices], display.engwaitforsingleobject, gdifncs_12c16d6b-ff3f-4cd4-8d4c-150ab8377dfb.xml, winddi/EngWaitForSingleObject
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
 - EngWaitForSingleObject
 - winddi/EngWaitForSingleObject
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
 - EngWaitForSingleObject
---

# EngWaitForSingleObject function


## -description

The <b>EngWaitForSingleObject</b> function puts the current thread of the display driver into a wait state until the specified event object is set to the signaled state, or until the wait times out.

## -parameters

### -param pEvent [in]

Pointer to an initialized event object. This event object handle was obtained in a previous call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>.

### -param pTimeOut [in]

(<i>Optional</i>) Pointer to a time-out value that specifies the absolute or relative time at which the wait is to be completed. A negative value specifies an interval relative to the current time. The value should be expressed in units of 100 nanoseconds. Absolute expiration times track any changes in the system time; relative expiration times are not affected by system time changes. If <i>pTimeOut</i> is <b>NULL</b>, the calling thread remains in a waiting state until the event object is signaled.

## -returns

<b>EngWaitForSingleObject</b> returns <b>TRUE</b> upon success, which includes the occurrence of a time-out. Otherwise, it returns <b>FALSE</b>. A return value of <b>FALSE</b> indicates that one of the parameters is invalid.

## -remarks

<b>EngWaitForSingleObject</b> causes a display driver thread to be put into a wait state. The display driver thread stays in the wait state until either the event object is set to the signaled state or until the wait times out. If no time-out value is supplied, the display driver thread remains in the wait state until the event object is set to the signaled state.

A synchronization event is automatically reset to the nonsignaled state when the wait is satisfied. Thus, only one wait will be satisfied per call to <a href="/windows/desktop/api/winddi/nf-winddi-engsetevent">EngSetEvent</a> or <a href="/windows-hardware/drivers/ddi/content/video/nf-video-videoportsetevent">VideoPortSetEvent</a>. In contrast, a notification event will not be automatically reset.

A time-out value of zero allows the driver to test the wait condition and to conditionally perform any side effects provided that the wait can be immediately satisfied.

The display driver can synchronize drawing operations between itself and the video miniport driver by calling <b>EngWaitForSingleObject</b> with an event object, and waiting until the miniport driver sets the event object to the signaled state.

The driver cannot call <b>EngWaitForSingleObject</b> on events returned from <a href="/windows/desktop/api/winddi/nf-winddi-engmapevent">EngMapEvent</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreateevent">EngCreateEvent</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engsetevent">EngSetEvent</a>



<a href="/windows-hardware/drivers/ddi/content/video/nf-video-videoportsetevent">VideoPortSetEvent</a>