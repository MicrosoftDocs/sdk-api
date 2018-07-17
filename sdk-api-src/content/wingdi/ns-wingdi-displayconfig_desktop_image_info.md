---
UID: NS:wingdi.DISPLAYCONFIG_DESKTOP_IMAGE_INFO
title: DISPLAYCONFIG_DESKTOP_IMAGE_INFO
author: windows-sdk-content
description: The DISPLAYCONFIG_DESKTOP_IMAGE_INFO structure contains information about the image displayed on the desktop.
old-location: display\displayconfig_desktop_image_info.htm
old-project: display
ms.assetid: 2DACA175-19BC-4192-A2FF-CB8AC7220B98
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: DISPLAYCONFIG_DESKTOP_IMAGE_INFO, DISPLAYCONFIG_DESKTOP_IMAGE_INFO structure [Display Devices], display.displayconfig_desktop_image_info, wingdi/DISPLAYCONFIG_DESKTOP_IMAGE_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 10 Client.
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
tech.root: 
req.typenames: DISPLAYCONFIG_DESKTOP_IMAGE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_DESKTOP_IMAGE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DISPLAYCONFIG_DESKTOP_IMAGE_INFO structure


## -description


The DISPLAYCONFIG_DESKTOP_IMAGE_INFO structure contains information about the image displayed on the desktop.


## -struct-fields




### -field PathSourceSize

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies the size of the VidPn source surface that is being displayed on the monitor.


### -field DesktopImageRegion

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines where the desktop image will be positioned within path source. 	Region must be completely inside the bounds of the path source size.


### -field DesktopImageClip

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that defines which part of the desktop image for this clone group will be displayed on this path. This currently must be set to the desktop size.

