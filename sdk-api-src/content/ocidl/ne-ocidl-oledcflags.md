---
UID: NE:ocidl.tagOLEDCFLAGS
title: OLEDCFLAGS
author: windows-sdk-content
description: Specifies additional information to the container about the device context that the object has requested.
old-location: com\oledcflags.htm
tech.root: com
ms.assetid: f8953376-2cbb-4f03-8216-2727d6a9f128
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OLEDCFLAGS, OLEDCFLAGS enumeration [COM], OLEDC_NODRAW, OLEDC_OFFSCREEN, OLEDC_PAINTBKGND, _ole_OLEDCFLAGS, com.oledcflags, ocidl/OLEDCFLAGS, ocidl/OLEDC_NODRAW, ocidl/OLEDC_OFFSCREEN, ocidl/OLEDC_PAINTBKGND
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ocidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - OLEDCFLAGS
product: Windows
targetos: Windows
req.typenames: OLEDCFLAGS
req.redist: 
---

# OLEDCFLAGS enumeration


## -description


Specifies additional information to the container about the device context that the object has requested.


## -enum-fields




### -field OLEDC_NODRAW

Indicates that the object will not use the returned <b>HDC</b> for drawing but merely to get information about the display device. In this case, the container can simply pass the window's device context without further processing.


### -field OLEDC_PAINTBKGND

Requests that the container paint the background behind the object before returning the device context. Objects should use this flag when requesting a device context to paint a transparent area.


### -field OLEDC_OFFSCREEN

Indicates that the object prefers to draw into an offscreen device context that should then be copied to the screen. The container can honor this request or not. If this bit is cleared, the container must return an on-screen device context allowing the object to perform direct screen operations such as showing a selection through an XOR operation. An object can specify this value when the drawing operation generates a lot of screen flicker.


## -see-also




<a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>
 

 

