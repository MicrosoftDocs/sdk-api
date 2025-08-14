---
UID: NF:winddi.EngMapEvent
title: EngMapEvent function (winddi.h)
description: The EngMapEvent function maps a user-mode event object to kernel mode.
helpviewer_keywords: ["EngMapEvent","EngMapEvent function [Display Devices]","display.engmapevent","gdifncs_5d41fd21-c767-4c7b-8bd6-546be9ce1439.xml","winddi/EngMapEvent"]
old-location: display\engmapevent.htm
tech.root: display
ms.assetid: a48f2367-49da-4d5c-87e5-b5c67e2311eb
ms.date: 12/05/2018
ms.keywords: EngMapEvent, EngMapEvent function [Display Devices], display.engmapevent, gdifncs_5d41fd21-c767-4c7b-8bd6-546be9ce1439.xml, winddi/EngMapEvent
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
 - EngMapEvent
 - winddi/EngMapEvent
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
 - EngMapEvent
---

# EngMapEvent function


## -description

The <b>EngMapEvent</b> function maps a user-mode event object to kernel mode.

## -parameters

### -param hDev [in]

Handle to the physical device associated with the event. This is the GDI handle passed as the <i>hdev</i> parameter to the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a> function.

### -param hUserObject [in]

Handle to the user-mode event to be mapped.

### -param Reserved1

Is reserved for system use, and must be set to <b>NULL</b>.

### -param Reserved2

Is reserved for system use, and must be set to <b>NULL</b>.

### -param Reserved3

Is reserved for system use, and must be set to <b>NULL</b>.

## -returns

<b>EngMapEvent</b> returns a pointer to an event object on success. Otherwise, it returns <b>NULL</b>.

## -remarks

After successfully mapping the user event, <b>EngMapEvent</b> automatically sets the event object to the signaled state, attempts to satisfy as many waits as possible, and then resets the event object to the nonsignaled state.

A mapped event provides a mechanism by which an application can wait for a kernel-mode graphics operation to complete. The display driver or video miniport driver signals the application when it is done using the resource for which the event was mapped, thus freeing the application to use the resource.

Display and miniport drivers cannot wait for mapped events, but can set or clear them.

The driver can also perform its own cleanup by calling <a href="/windows/desktop/api/winddi/nf-winddi-engunmapevent">EngUnmapEvent</a> on the event object returned by <b>EngMapEvent</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunmapevent">EngUnmapEvent</a>