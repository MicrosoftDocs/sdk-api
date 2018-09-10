---
UID: NF:winddi.EngReadStateEvent
title: EngReadStateEvent function
author: windows-sdk-content
description: The EngReadStateEvent function returns the current state of the specified event object:\_signaled or nonsignaled.
old-location: display\engreadstateevent.htm
tech.root: display
ms.assetid: 32dddcc0-4cf2-467f-b1a6-03c9892d3473
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngReadStateEvent, EngReadStateEvent function [Display Devices], display.engreadstateevent, gdifncs_921fb236-706b-405c-affd-25811f97c7de.xml, winddi/EngReadStateEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - EngReadStateEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngReadStateEvent function


## -description


The <b>EngReadStateEvent</b> function returns the current state of the specified event object: signaled or nonsignaled.


## -parameters




### -param pEvent [in]

Pointer to the event object returned by a previous call to <a href="https://msdn.microsoft.com/0fe4c840-ba85-492c-ac3d-b7c8639d1210">EngCreateEvent</a> or <a href="https://msdn.microsoft.com/a48f2367-49da-4d5c-87e5-b5c67e2311eb">EngMapEvent</a>.


## -returns



<b>EngReadStateEvent</b> returns a nonzero value if the event object is currently set to the signaled state. If the event object is set to the nonsignaled state, this function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/0fe4c840-ba85-492c-ac3d-b7c8639d1210">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/a48f2367-49da-4d5c-87e5-b5c67e2311eb">EngMapEvent</a>
 

 

