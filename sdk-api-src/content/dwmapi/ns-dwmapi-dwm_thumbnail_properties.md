---
UID: NS:dwmapi._DWM_THUMBNAIL_PROPERTIES
title: DWM_THUMBNAIL_PROPERTIES (dwmapi.h)
description: Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the DwmUpdateThumbnailProperties function.
helpviewer_keywords: ["*PDWM_THUMBNAIL_PROPERTIES","DWM_THUMBNAIL_PROPERTIES","DWM_THUMBNAIL_PROPERTIES structure [Desktop Window Manager]","PDWM_THUMBNAIL_PROPERTIES","PDWM_THUMBNAIL_PROPERTIES structure pointer [Desktop Window Manager]","_udwm_dwm_thumbnail_properties","_udwm_dwm_thumbnail_properties_cpp","dwm.dwm_thumbnail_properties","dwmapi/DWM_THUMBNAIL_PROPERTIES","dwmapi/PDWM_THUMBNAIL_PROPERTIES","winui._udwm_dwm_thumbnail_properties"]
old-location: dwm\dwm_thumbnail_properties.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\dwm_thumbnail_properties.htm
ms.date: 12/05/2018
ms.keywords: '*PDWM_THUMBNAIL_PROPERTIES, DWM_THUMBNAIL_PROPERTIES, DWM_THUMBNAIL_PROPERTIES structure [Desktop Window Manager], PDWM_THUMBNAIL_PROPERTIES, PDWM_THUMBNAIL_PROPERTIES structure pointer [Desktop Window Manager], _udwm_dwm_thumbnail_properties, _udwm_dwm_thumbnail_properties_cpp, dwm.dwm_thumbnail_properties, dwmapi/DWM_THUMBNAIL_PROPERTIES, dwmapi/PDWM_THUMBNAIL_PROPERTIES, winui._udwm_dwm_thumbnail_properties'
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
targetos: Windows
req.typenames: DWM_THUMBNAIL_PROPERTIES, *PDWM_THUMBNAIL_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DWM_THUMBNAIL_PROPERTIES
 - dwmapi/_DWM_THUMBNAIL_PROPERTIES
 - PDWM_THUMBNAIL_PROPERTIES
 - dwmapi/PDWM_THUMBNAIL_PROPERTIES
 - DWM_THUMBNAIL_PROPERTIES
 - dwmapi/DWM_THUMBNAIL_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWM_THUMBNAIL_PROPERTIES
---

# DWM_THUMBNAIL_PROPERTIES structure


## -description

Specifies Desktop Window Manager (DWM) thumbnail properties. Used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmupdatethumbnailproperties">DwmUpdateThumbnailProperties</a> function.

## -struct-fields

### -field dwFlags

A bitwise combination of <a href="/windows/desktop/dwm/dwm-tnp-constants">DWM thumbnail constant</a> values that indicates which members of this structure are set.

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