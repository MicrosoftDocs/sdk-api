---
UID: NF:winddi.EngClearEvent
title: EngClearEvent function
author: windows-sdk-content
description: The EngClearEvent function sets a specified event object to the nonsignaled state.
old-location: display\engclearevent.htm
old-project: display
ms.assetid: fa87ed4f-4ccb-465c-bcd5-890694b790a3
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngClearEvent, EngClearEvent function [Display Devices], display.engclearevent, gdifncs_0650b2ea-0f64-425b-bfd4-a7c369f2915b.xml, winddi/EngClearEvent
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
 - EngClearEvent
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngClearEvent function


## -description


The <b>EngClearEvent</b> function sets a specified event object to the nonsignaled state.


## -parameters




### -param pEvent [in]

Pointer to the event object returned by a previous call to either <a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564211">EngCreateEvent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564970">EngMapEvent</a>
 

 

