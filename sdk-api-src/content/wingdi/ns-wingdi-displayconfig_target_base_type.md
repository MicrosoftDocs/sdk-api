---
UID: NS:wingdi.DISPLAYCONFIG_TARGET_BASE_TYPE
title: DISPLAYCONFIG_TARGET_BASE_TYPE
author: windows-sdk-content
description: Specifies base output technology info for a given target ID.
old-location: display\displayconfig_target_base_type.htm
old-project: display
ms.assetid: 7916E714-9A3C-4682-AC08-9B6EE222D8B7
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DISPLAYCONFIG_TARGET_BASE_TYPE, DISPLAYCONFIG_TARGET_BASE_TYPE structure [Display Devices], display.displayconfig_target_base_type, wingdi/DISPLAYCONFIG_TARGET_BASE_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: DISPLAYCONFIG_TARGET_BASE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_TARGET_BASE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DISPLAYCONFIG_TARGET_BASE_TYPE structure


## -description


Specifies base output technology info for a given target ID.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/2fdfa54e-2a5f-448f-98e3-e51ce0acaeaf">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains info about the request for the target device name. The caller should set the <b>type</b> member of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to <b>DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE</b> and the <b>adapterId</b> and <b>id</b> members of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to the target for which the caller wants the target device name.

 The caller should set the <b>size</b> member of <a href="https://msdn.microsoft.com/2fdfa54e-2a5f-448f-98e3-e51ce0acaeaf">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> to at least the size of the <b>DISPLAYCONFIG_TARGET_BASE_TYPE</b> structure.


### -field baseOutputTechnology

The base output technology, given as a constant value of the <a href="https://msdn.microsoft.com/f8c2095a-d67e-42ed-b615-b5e0e0e0d507">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a> enumeration, of the adapter and the target specified by the <b>header</b> member. See Remarks.


## -remarks



For a Miracast display device, a call to the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a>  function always returns  a value of <a href="https://msdn.microsoft.com/f8c2095a-d67e-42ed-b615-b5e0e0e0d507">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>.<b>DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST</b>, regardless of what the Miracast sink reports as the connector type.




## -see-also




<a href="https://msdn.microsoft.com/2fdfa54e-2a5f-448f-98e3-e51ce0acaeaf">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/f8c2095a-d67e-42ed-b615-b5e0e0e0d507">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>



<a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a>
 

 

