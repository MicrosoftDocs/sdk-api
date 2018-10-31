---
UID: NF:joystickapi.joyConfigChanged
title: joyConfigChanged function
author: windows-sdk-content
description: The joyConfigChanged function informs the joystick driver that the configuration has changed and should be reloaded from the registry.
old-location: multimedia\joyconfigchanged.htm
tech.root: Multimedia
ms.assetid: 3cdc7888-2d66-4fb9-abad-86e891f4ebe4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_joyConfigChanged, joyConfigChanged, joyConfigChanged function [Windows Multimedia], joystickapi/joyConfigChanged, multimedia.joyconfigchanged"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: joystickapi.h
req.include-header: Dinput.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-joystick-l1-1-0.dll
 - winmmbase.dll
api_name:
 - joyConfigChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# joyConfigChanged function


## -description



The <b>joyConfigChanged</b> function informs the joystick driver that the configuration has changed and should be reloaded from the registry.




## -parameters




### -param dwFlags

Reserved for future use. Must equal zero.


## -returns



Returns JOYERR_NOERROR if successful. Returns JOYERR_PARMS if the parameter is non-zero.




## -remarks



This function causes a window message to be sent to all top-level windows. This message may be defined by applications that need to respond to changes in joystick calibration by using <b>RegisterWindowMessage</b> with the following message ID:


```cpp

#define JOY_CONFIGCHANGED_MSGSTRING     "MSJSTICK_VJOYD_MSGSTR"

```





## -see-also




<a href="https://msdn.microsoft.com/29fe25c8-51ea-4dc1-9f98-1c10d23b7b2a">Joysticks</a>



<a href="https://msdn.microsoft.com/84e47ac3-b40f-48bc-8f59-cc678d7d521e">Multimedia Joystick Functions</a>
 

 

