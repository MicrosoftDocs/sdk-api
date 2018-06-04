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

# DIJOYCONFIG structure


## -description


The DIJOYCONFIG structure contains information about a joystick's configuration. 


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field guidInstance

Specifies the instance GUID for the joystick. 


### -field hwc

Joystick hardware configuration. 


### -field dwGain

Specifies the global gain setting. This value is applied to all force feedback effects as a "master volume control". 


### -field wszType

The joystick type for the joystick. It must be one of the values enumerated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff540987">IDirectInputJoyConfig8::EnumTypes</a>. 


### -field wszCallout

The callout driver for the joystick. 


### -field guidGameport

Specifies a GUID that identifies the gameport being used for this joystick.


## -remarks



WDM gameports can be found during enumeration by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff540989">IDirectInputJoyConfig8::GetTypeInfo</a> method for an enumerated joystick, then studying the flags present in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538513">DIJOYTYPEINFO</a> structure. If the JOY_HWS_ISGAMEPORTBUS flag is set, the currently enumerated object is an available WDM gameport.



