---
UID: NF:joystickapi.joyGetNumDevs
title: joyGetNumDevs function (joystickapi.h)
author: windows-sdk-content
description: The joyGetNumDevs function queries the joystick driver for the number of joysticks it supports.
old-location: multimedia\joygetnumdevs.htm
tech.root: Multimedia
ms.assetid: dc268db5-da2d-4139-97da-5d56a54287d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_joyGetNumDevs, joyGetNumDevs, joyGetNumDevs function [Windows Multimedia], joystickapi/joyGetNumDevs, multimedia.joygetnumdevs"
ms.topic: function
req.header: joystickapi.h
req.include-header: Windows.h
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
 - joyGetNumDevs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# joyGetNumDevs function


## -description



The <b>joyGetNumDevs</b> function queries the joystick driver for the number of joysticks it supports.




## -parameters






## -returns



The <b>joyGetNumDevs</b> function returns the number of joysticks supported by the current driver or zero if no driver is installed.




## -remarks



Use the <a href="https://docs.microsoft.com/previous-versions//dd757107(v=vs.85)">joyGetPos</a> function to determine whether a given joystick is physically attached to the system. If the specified joystick is not connected, <b>joyGetPos</b> returns a JOYERR_UNPLUGGED error value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>
 

 

