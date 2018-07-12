---
UID: NF:winddi.EngReadStateEvent
title: EngReadStateEvent function
author: windows-sdk-content
description: The EngReadStateEvent function returns the current state of the specified event object:\_signaled or nonsignaled.
old-location: display\engreadstateevent.htm
old-project: display
ms.assetid: 32dddcc0-4cf2-467f-b1a6-03c9892d3473
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngReadStateEvent, EngReadStateEvent function [Display Devices], display.engreadstateevent, gdifncs_921fb236-706b-405c-affd-25811f97c7de.xml, winddi/EngReadStateEvent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngReadStateEvent function


## -description


The <b>EngReadStateEvent</b> function returns the current state of the specified event object: signaled or nonsignaled.


## -parameters




### -param pEvent [in]

Pointer to the event object returned by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.


## -returns



<b>EngReadStateEvent</b> returns a nonzero value if the event object is currently set to the signaled state. If the event object is set to the nonsignaled state, this function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

