---
UID: NF:joystickapi.joyConfigChanged
title: joyConfigChanged function (joystickapi.h)
description: The joyConfigChanged function informs the joystick driver that the configuration has changed and should be reloaded from the registry.
helpviewer_keywords: ["_win32_joyConfigChanged","joyConfigChanged","joyConfigChanged function [Windows Multimedia]","joystickapi/joyConfigChanged","multimedia.joyconfigchanged"]
old-location: multimedia\joyconfigchanged.htm
tech.root: Multimedia
ms.assetid: 3cdc7888-2d66-4fb9-abad-86e891f4ebe4
ms.date: 12/05/2018
ms.keywords: _win32_joyConfigChanged, joyConfigChanged, joyConfigChanged function [Windows Multimedia], joystickapi/joyConfigChanged, multimedia.joyconfigchanged
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - joyConfigChanged
 - joystickapi/joyConfigChanged
dev_langs:
 - c++
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

<a href="/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>