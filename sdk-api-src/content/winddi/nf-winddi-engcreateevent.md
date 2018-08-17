---
UID: NF:winddi.EngCreateEvent
title: EngCreateEvent function
author: windows-sdk-content
description: The EngCreateEvent function creates a synchronization event object that can be used to synchronize hardware access between a display driver and the video miniport driver.
old-location: display\engcreateevent.htm
old-project: display
ms.assetid: 0fe4c840-ba85-492c-ac3d-b7c8639d1210
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngCreateEvent, EngCreateEvent function [Display Devices], display.engcreateevent, gdifncs_d8f6efc2-d0a2-4790-88c5-16e4487e2ce2.xml, winddi/EngCreateEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
 - EngCreateEvent
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/b1db14ed-345f-428e-9338-74c7b230e661">EngDeleteEvent</a>



<a href="https://msdn.microsoft.com/04e5d5e0-02b1-4335-9830-ecf04fdc0db1">EngSetEvent</a>



<a href="https://msdn.microsoft.com/a2a1c7ad-1e56-45f7-83de-49ebc0d831f9">EngWaitForSingleObject</a>
 

 

