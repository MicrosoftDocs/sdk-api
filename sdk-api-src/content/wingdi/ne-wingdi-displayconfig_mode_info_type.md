---
UID: NE:wingdi.__unnamed_enum_4
title: DISPLAYCONFIG_MODE_INFO_TYPE (wingdi.h)
author: windows-sdk-content
description: The DISPLAYCONFIG_MODE_INFO_TYPE enumeration specifies that the information that is contained within the DISPLAYCONFIG_MODE_INFO structure is either source or target mode.
old-location: display\displayconfig_mode_info_type.htm
tech.root: display
ms.assetid: d5ddb1d5-6b74-471f-86f0-fee72f30b648
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_e8e863ac-c37b-4818-a968-e2658c3103e1.xml, DISPLAYCONFIG_MODE_INFO_TYPE, DISPLAYCONFIG_MODE_INFO_TYPE enumeration [Display Devices], DISPLAYCONFIG_MODE_INFO_TYPE_DESKTOP_IMAGE, DISPLAYCONFIG_MODE_INFO_TYPE_FORCE_UINT32, DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE, DISPLAYCONFIG_MODE_INFO_TYPE_TARGET, display.displayconfig_mode_info_type, wingdi/DISPLAYCONFIG_MODE_INFO_TYPE, wingdi/DISPLAYCONFIG_MODE_INFO_TYPE_DESKTOP_IMAGE, wingdi/DISPLAYCONFIG_MODE_INFO_TYPE_FORCE_UINT32, wingdi/DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE, wingdi/DISPLAYCONFIG_MODE_INFO_TYPE_TARGET
ms.topic: enum
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Windows Client.
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
 - DISPLAYCONFIG_MODE_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_MODE_INFO_TYPE
req.redist: 
---

# DISPLAYCONFIG_MODE_INFO_TYPE enumeration


## -description


The DISPLAYCONFIG_MODE_INFO_TYPE enumeration specifies that the information that is contained within the <a href="https://msdn.microsoft.com/39ffe49b-96d3-4d8b-94a7-01c388448b82">DISPLAYCONFIG_MODE_INFO</a> structure is either source or target mode.


## -enum-fields




### -field DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE

Indicates that the <a href="https://msdn.microsoft.com/39ffe49b-96d3-4d8b-94a7-01c388448b82">DISPLAYCONFIG_MODE_INFO</a> structure contains source mode information.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_TARGET

Indicates that the <a href="https://msdn.microsoft.com/39ffe49b-96d3-4d8b-94a7-01c388448b82">DISPLAYCONFIG_MODE_INFO</a> structure contains target mode information.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_DESKTOP_IMAGE

Indicates that the <a href="https://msdn.microsoft.com/39ffe49b-96d3-4d8b-94a7-01c388448b82">DISPLAYCONFIG_MODE_INFO</a> structure contains a valid <a href="https://msdn.microsoft.com/2DACA175-19BC-4192-A2FF-CB8AC7220B98">DISPLAYCONFIG_DESKTOP_IMAGE_INFO</a> structure. Supported starting in Windows 10.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://msdn.microsoft.com/39ffe49b-96d3-4d8b-94a7-01c388448b82">DISPLAYCONFIG_MODE_INFO</a>
 

 

