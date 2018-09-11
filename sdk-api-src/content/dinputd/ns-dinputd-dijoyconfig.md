---
UID: NS:dinputd.DIJOYCONFIG
title: DIJOYCONFIG
author: windows-sdk-content
description: The DIJOYCONFIG structure contains information about a joystick's configuration.
old-location: hid\dijoyconfig.htm
tech.root: hid
ms.assetid: 2b17432f-fa5e-4ce3-9814-c24a45a49343
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*LPDIJOYCONFIG, DIJOYCONFIG, DIJOYCONFIG structure [Human Input Devices], di_ref_dc34a740-8987-4012-9e22-e59de2544445.xml, dinputd/DIJOYCONFIG, hid.dijoyconfig"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIJOYCONFIG
product: Windows
targetos: Windows
req.typenames: DIJOYCONFIG, *LPDIJOYCONFIG
req.redist: 
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

The joystick type for the joystick. It must be one of the values enumerated by <a href="https://msdn.microsoft.com/bacca5a8-2323-46d7-b018-cce2f09bb06d">IDirectInputJoyConfig8::EnumTypes</a>. 


### -field wszCallout

The callout driver for the joystick. 


### -field guidGameport

Specifies a GUID that identifies the gameport being used for this joystick.


## -remarks



WDM gameports can be found during enumeration by calling <a href="https://msdn.microsoft.com/e850c3a4-b2dd-4de5-82e3-5bbd90a7ba15">IDirectInputJoyConfig8::GetTypeInfo</a> method for an enumerated joystick, then studying the flags present in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/54f52839-59ed-4edd-8d28-e3504f9900d0">DIJOYTYPEINFO</a> structure. If the JOY_HWS_ISGAMEPORTBUS flag is set, the currently enumerated object is an available WDM gameport.



