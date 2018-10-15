---
UID: NS:winuser.tagPOINTER_DEVICE_INFO
title: tagPOINTER_DEVICE_INFO
author: windows-sdk-content
description: Contains information about a pointer device. An array of these structures is returned from the GetPointerDevices function. A single structure is returned from a call to the GetPointerDevice function.
old-location: input_pointerdevice\pointer_device_info.htm
tech.root: Input_PointerDevice
ms.assetid: 1b909caf-2d69-42b9-8d60-5d89a0286f59
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: POINTER_DEVICE_INFO, POINTER_DEVICE_INFO structure, input_pointerdevice.pointer_device_info, tagPOINTER_DEVICE_INFO, unifiedinputstack.pointer_device_info, winuser/POINTER_DEVICE_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Winuser.h
api_name:
 - POINTER_DEVICE_INFO
product: Windows
targetos: Windows
req.typenames: POINTER_DEVICE_INFO
req.redist: 
---

# tagPOINTER_DEVICE_INFO structure


## -description


Contains information about a pointer device. An array of these structures is returned  from the <a href="https://msdn.microsoft.com/91FD5EBA-EDD7-4D7D-ABF3-3CE2461417B0">GetPointerDevices</a> function. A single structure is returned from a call to the <a href="https://msdn.microsoft.com/800E0BFE-6E57-4EAA-B47C-FEEC0B5BFA2F">GetPointerDevice</a> function. 


## -struct-fields




### -field displayOrientation

 One of the values from <a href="https://msdn.microsoft.com/82709d44-45e6-47ec-9caa-5a947a568c52">DISPLAYCONFIG_ROTATION</a>, which identifies the orientation of the input digitizer.

<div class="alert"><b>Note</b>  This value is 0 when the source of input is <a href="https://msdn.microsoft.com/9B82898C-92DF-4F12-9440-D3D5CFD4D0A0">Touch Injection</a>.</div>
<div> </div>

### -field device

The handle to the pointer device.


### -field pointerDeviceType

The device type.


### -field monitor

The HMONITOR for the display that the device is mapped to. This is not necessarily the monitor that the pointer device is physically connected to.


### -field startingCursorId

The lowest ID that's assigned to the device.


### -field maxActiveContacts

The number of supported simultaneous contacts.


### -field productString

The string that identifies the product.


## -see-also




<a href="https://msdn.microsoft.com/33DCB172-8D95-4205-AE2E-ADD7F3BF988A">Structures</a>
 

 

