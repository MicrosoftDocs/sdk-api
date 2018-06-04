---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# WINNLSEnableIME function


## -description


Temporarily enables or disables an Input Method Editor (IME) and, at the same time, turns on or off the display of all windows owned by the IME.
        
            
<div class="alert"><b>Note</b>  This function is obsolete and should not be used.</div><div> </div>

## -parameters




### -param HWND

TBD


### -param BOOL

TBD




#### - bFlag [in]

<b>TRUE</b> to enable the IME; <b>FALSE</b> to disable.


#### - hwnd [in]

Must be <b>NULL</b>. Specifying a particular IME for each application is not supported.


## -returns



The previous state of the IME. <b>TRUE</b> if it was enabled before this call, otherwise, <b>FALSE</b>.




## -remarks



The terms "enabled" and "disabled" in regard to this function are defined as follows:
            
                

If an IME is disabled, <a href="https://msdn.microsoft.com/399a567c-b34d-48f5-9bd5-7e3ecc01c1a9">IME_WINDOWUPDATE(FALSE)</a> is issued to the IME, which responds by deleting the conversion and system windows. With the IME disabled, keyboard messages are not sent to the IME, but are sent directly to the application. Even if the IME is disabled, the API that uses the <a href="https://msdn.microsoft.com/f1e6e73b-53f7-456e-b6a9-61841b83c909">SendIMEMessageEx</a> function is still valid.

If an IME is enabled, <a href="https://msdn.microsoft.com/399a567c-b34d-48f5-9bd5-7e3ecc01c1a9">IME_WINDOWUPDATE(TRUE)</a> is issued to the IME, which responds by redisplaying the conversion and system windows. With the IME enabled, keyboard messages are sent to the IME.



