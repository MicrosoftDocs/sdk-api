---
UID: NF:winddi.EngUnmapEvent
title: EngUnmapEvent function
author: windows-sdk-content
description: The EngUnmapEvent function cleans up the kernel-mode resources allocated for a mapped user-mode event.
old-location: display\engunmapevent.htm
old-project: display
ms.assetid: 3be72e38-e7ea-407b-87e4-c6293d6160f6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngUnmapEvent, EngUnmapEvent function [Display Devices], display.engunmapevent, gdifncs_0f5f2320-13d2-471a-93b6-739f9ecbd620.xml, winddi/EngUnmapEvent
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
 - EngUnmapEvent
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngUnmapEvent function


## -description


The <b>EngUnmapEvent</b> function cleans up the kernel-mode resources allocated for a mapped user-mode event.


## -parameters




### -param pEvent [in]

Pointer to an event object returned from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.


## -returns



<b>EngUnmapEvent</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



The display driver should call <b>EngUnmapEvent</b> when it is notified that the process (typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff564207">EngCreateDriverObj</a>) that created the user-mode event has terminated. The display driver can also call <b>EngUnmapEvent</b> to perform its own cleanup. The display and miniport drivers should not touch the event object after <b>EngUnmapEvent</b> has been called.

The display driver can call <b>EngUnmapEvent</b> only for an event object returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>. It must not call this function for an event object returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564207">EngCreateDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

