---
UID: NE:wingdi.__unnamed_enum_6
title: DISPLAYCONFIG_DEVICE_INFO_TYPE (wingdi.h)
author: windows-sdk-content
description: The DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration specifies the type of display device info to configure or obtain through the DisplayConfigSetDeviceInfo or DisplayConfigGetDeviceInfo function.
old-location: display\displayconfig_device_info_type.htm
tech.root: display
ms.assetid: 40cc67c0-1508-4b67-b297-5a8dabaabb16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_29e89f4b-f002-4493-a1dc-5dba3150a7f8.xml, DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32, DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME, DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE, DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION, DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE, DISPLAYCONFIG_DEVICE_INFO_TYPE, DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration [Display Devices], display.displayconfig_device_info_type, wingdi/DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME, wingdi/DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE, wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION, wingdi/DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE, wingdi/DISPLAYCONFIG_DEVICE_INFO_TYPE
ms.topic: enum
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
 - wingdi.h
api_name:
 - DISPLAYCONFIG_DEVICE_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_DEVICE_INFO_TYPE
req.redist: 
ms.custom: 19H1
---

# DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration


## -description


The DISPLAYCONFIG_DEVICE_INFO_TYPE enumeration specifies the type of display device info to configure or obtain through the <a href="https://msdn.microsoft.com/4050b1f0-a588-427c-a0df-eefdc488fc20">DisplayConfigSetDeviceInfo</a> or <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function.


## -enum-fields




### -field DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME

Specifies the source name of the display device. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns the source name in the <a href="https://msdn.microsoft.com/92813ffc-1915-4f26-afb1-936bf76f7844">DISPLAYCONFIG_SOURCE_DEVICE_NAME</a> structure.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME

Specifies information about the monitor. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns info about the monitor in the <a href="https://msdn.microsoft.com/85507b69-8ce0-4f39-a4d3-7d67f515b451">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE

Specifies information about the preferred mode of a monitor. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns info about the preferred mode of a monitor in the <a href="https://msdn.microsoft.com/1a4926ca-36d2-466c-b3d2-b59d34a89ee6">DISPLAYCONFIG_TARGET_PREFERRED_MODE</a> structure.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME

Specifies the graphics adapter name. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns the adapter name in the <a href="https://msdn.microsoft.com/248f325f-37ae-48f4-a758-ee78a3e3f0b8">DISPLAYCONFIG_ADAPTER_NAME</a> structure.


### -field DISPLAYCONFIG_DEVICE_INFO_SET_TARGET_PERSISTENCE

Specifies how to set the monitor. If the <a href="https://msdn.microsoft.com/4050b1f0-a588-427c-a0df-eefdc488fc20">DisplayConfigSetDeviceInfo</a> function is successful, <b>DisplayConfigSetDeviceInfo</b> uses info in the <a href="https://msdn.microsoft.com/4798a1e1-8685-40c2-917a-0ee071bc780c">DISPLAYCONFIG_SET_TARGET_PERSISTENCE</a> structure to force the output in a boot-persistent manner. 


### -field DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE

Specifies how to set the base output technology for a given target ID. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns base output technology info in the <a href="https://msdn.microsoft.com/7916E714-9A3C-4682-AC08-9B6EE222D8B7">DISPLAYCONFIG_TARGET_BASE_TYPE</a> structure.

Supported by WDDM 1.3 and later user-mode display drivers running on Windows 8.1 and later.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_SUPPORT_VIRTUAL_RESOLUTION

Specifies the state of virtual mode support. If the <a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> returns virtual mode support information in the <a href="https://msdn.microsoft.com/D9208D00-F437-4B2E-8C39-044F75088659">DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION</a> structure. Supported starting in Windows 10.


### -field DISPLAYCONFIG_DEVICE_INFO_SET_SUPPORT_VIRTUAL_RESOLUTION

Specifies how to set the state of virtual mode support. If the <a href="https://msdn.microsoft.com/4050b1f0-a588-427c-a0df-eefdc488fc20">DisplayConfigGetDeviceInfo</a> function is successful, <b>DisplayConfigGetDeviceInfo</b> uses info in the <a href="https://msdn.microsoft.com/D9208D00-F437-4B2E-8C39-044F75088659">DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION</a> structure to change the state of virtual mode support. Supported starting in Windows 10.


### -field DISPLAYCONFIG_DEVICE_INFO_GET_ADVANCED_COLOR_INFO


### -field DISPLAYCONFIG_DEVICE_INFO_SET_ADVANCED_COLOR_STATE


### -field DISPLAYCONFIG_DEVICE_INFO_GET_SDR_WHITE_LEVEL


### -field DISPLAYCONFIG_DEVICE_INFO_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://msdn.microsoft.com/248f325f-37ae-48f4-a758-ee78a3e3f0b8">DISPLAYCONFIG_ADAPTER_NAME</a>



<a href="https://msdn.microsoft.com/4798a1e1-8685-40c2-917a-0ee071bc780c">DISPLAYCONFIG_SET_TARGET_PERSISTENCE</a>



<a href="https://msdn.microsoft.com/92813ffc-1915-4f26-afb1-936bf76f7844">DISPLAYCONFIG_SOURCE_DEVICE_NAME</a>



<a href="https://msdn.microsoft.com/7916E714-9A3C-4682-AC08-9B6EE222D8B7">DISPLAYCONFIG_TARGET_BASE_TYPE</a>



<a href="https://msdn.microsoft.com/85507b69-8ce0-4f39-a4d3-7d67f515b451">DISPLAYCONFIG_TARGET_DEVICE_NAME</a>



<a href="https://msdn.microsoft.com/1a4926ca-36d2-466c-b3d2-b59d34a89ee6">DISPLAYCONFIG_TARGET_PREFERRED_MODE</a>



<a href="https://msdn.microsoft.com/249dcb1a-4ce3-4478-8331-fb81e91313b0">DisplayConfigGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/4050b1f0-a588-427c-a0df-eefdc488fc20">DisplayConfigSetDeviceInfo</a>
 

 

