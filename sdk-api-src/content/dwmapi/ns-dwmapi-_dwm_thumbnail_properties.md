---
UID: NS:dwmapi._DWM_THUMBNAIL_PROPERTIES
title: "_DWM_THUMBNAIL_PROPERTIES"
author: windows-sdk-content
description: Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the DwmUpdateThumbnailProperties function.
old-location: dwm\dwm_thumbnail_properties.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_thumbnail_properties.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDWM_THUMBNAIL_PROPERTIES, DWM_THUMBNAIL_PROPERTIES, DWM_THUMBNAIL_PROPERTIES structure [Desktop Window Manager], PDWM_THUMBNAIL_PROPERTIES, PDWM_THUMBNAIL_PROPERTIES structure pointer [Desktop Window Manager], _DWM_THUMBNAIL_PROPERTIES, _udwm_dwm_thumbnail_properties, _udwm_dwm_thumbnail_properties_cpp, dwm.dwm_thumbnail_properties, dwmapi/DWM_THUMBNAIL_PROPERTIES, dwmapi/PDWM_THUMBNAIL_PROPERTIES, winui._udwm_dwm_thumbnail_properties"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Dwmapi.h
api_name:
 - DWM_THUMBNAIL_PROPERTIES
product: Windows
targetos: Windows
req.typenames: DWM_THUMBNAIL_PROPERTIES, *PDWM_THUMBNAIL_PROPERTIES
req.redist: 
---

# _DWM_THUMBNAIL_PROPERTIES structure


## -description


Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the <a href="https://msdn.microsoft.com/02c40cda-b87c-44c5-bcc5-3d0e83b7b14b">DwmUpdateThumbnailProperties</a> function.


## -struct-fields




### -field dwFlags

A bitwise combination of <a href="https://msdn.microsoft.com/8eee1baf-e24e-40af-92ab-a7acae267ecc">DWM thumbnail constant</a> values that indicates which members of this structure are set.


### -field rcDestination

The area in the destination window where the thumbnail will be rendered.


### -field rcSource

The region of the source window to use as the thumbnail. By default, the entire window is used as the thumbnail.


### -field opacity

The opacity with which to render the thumbnail. 0 is fully transparent while 255 is fully opaque. The default value is 255.


### -field fVisible

<b>TRUE</b> to make the thumbnail visible; otherwise, <b>FALSE</b>. The default is <b>FALSE</b>.


### -field fSourceClientAreaOnly

<b>TRUE</b> to use only the thumbnail source's client area; otherwise, <b>FALSE</b>. The default is <b>FALSE</b>.

