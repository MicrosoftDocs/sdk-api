---
UID: NF:winddi.EngDeleteEvent
title: EngDeleteEvent function
author: windows-sdk-content
description: The EngDeleteEvent function deletes the specified event object.
old-location: display\engdeleteevent.htm
old-project: display
ms.assetid: b1db14ed-345f-428e-9338-74c7b230e661
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngDeleteEvent, EngDeleteEvent function [Display Devices], display.engdeleteevent, gdifncs_8a703ede-e100-493c-8ede-82c03361633f.xml, winddi/EngDeleteEvent
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
 - EngDeleteEvent
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteEvent function


## -description


The <b>EngDeleteEvent</b> function deletes the specified event object.


## -parameters




### -param pEvent [in]

Pointer to the event object to be deleted.


## -returns



<b>EngDeleteEvent</b> returns <b>TRUE</b> if it is successful in deleting the specified event object. It returns <b>FALSE</b> if the caller attempts to delete a mapped user event.




## -remarks



A display driver can call <b>EngDeleteEvent</b> only with an event object returned from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a> function, and must not call it to delete event objects returned from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.

Before calling <b>EngDeleteEvent</b>, the display driver must notify all holders of the specified event object that it is about to become invalid.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

