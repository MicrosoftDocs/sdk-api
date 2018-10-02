---
UID: NE:shellscalingapi.MONITOR_DPI_TYPE
title: MONITOR_DPI_TYPE
author: windows-sdk-content
description: Identifies the dots per inch (dpi) setting for a monitor.
old-location: hidpi\monitor_dpi_type_enumeration.htm
tech.root: hidpi
ms.assetid: 9022A1E1-CB99-4278-A3BD-171E26708DBD
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MDT_ANGULAR_DPI, MDT_DEFAULT, MDT_EFFECTIVE_DPI, MDT_RAW_DPI, MONITOR_DPI_TYPE, MONITOR_DPI_TYPE enumeration, MONITOR_DPI_TYPE enumeration enumeration [High DPI], hidpi.monitor_dpi_type_enumeration, shellscalingapi/MDT_ANGULAR_DPI, shellscalingapi/MDT_DEFAULT, shellscalingapi/MDT_EFFECTIVE_DPI, shellscalingapi/MDT_RAW_DPI, shellscalingapi/MONITOR_DPI_TYPE enumeration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - ShellScalingApi.h
api_name:
 - MONITOR_DPI_TYPE
product: Windows
targetos: Windows
req.typenames: MONITOR_DPI_TYPE
req.redist: 
---

# MONITOR_DPI_TYPE enumeration


## -description


Identifies the dots per inch (dpi) setting for a monitor.


## -enum-fields




### -field MDT_EFFECTIVE_DPI

The effective DPI. This value should be used when determining the correct scale factor for scaling UI elements. This incorporates the scale factor set by the user for this specific display.


### -field MDT_ANGULAR_DPI

The angular DPI. This DPI ensures rendering at a compliant angular resolution on the screen. This does not include the scale factor set by the user for this specific display.


### -field MDT_RAW_DPI

The raw DPI. This value is the linear DPI of the screen as measured on the screen itself. Use this value when you want to read the pixel density and not the recommended scaling setting. This does not include the scale factor set by the user for this specific display and is not guaranteed to be a supported DPI value.


### -field MDT_DEFAULT

The default DPI setting for a monitor is MDT_EFFECTIVE_DPI.


## -remarks



All of these settings are affected by the <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> of your application




## -see-also




<a href="https://msdn.microsoft.com/AB741D14-0BA1-4C33-91D8-1331BE96DE95">GetDpiForMonitor</a>
 

 

