---
UID: NS:wingdi.DISPLAYCONFIG_RATIONAL
title: DISPLAYCONFIG_RATIONAL (wingdi.h)
description: The DISPLAYCONFIG_RATIONAL structure describes a fractional value that represents vertical and horizontal frequencies of a video mode (that is, vertical sync and horizontal sync).
helpviewer_keywords: ["CCD_Structures_6b317b78-bbb5-4f49-9dee-2c9597c19957.xml","DISPLAYCONFIG_RATIONAL","DISPLAYCONFIG_RATIONAL structure [Display Devices]","display.displayconfig_rational","wingdi/DISPLAYCONFIG_RATIONAL"]
old-location: display\displayconfig_rational.htm
tech.root: display
ms.assetid: 1f2f25f7-5ea1-46f4-ad9f-c50c367bb600
ms.date: 12/05/2018
ms.keywords: CCD_Structures_6b317b78-bbb5-4f49-9dee-2c9597c19957.xml, DISPLAYCONFIG_RATIONAL, DISPLAYCONFIG_RATIONAL structure [Display Devices], display.displayconfig_rational, wingdi/DISPLAYCONFIG_RATIONAL
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
targetos: Windows
req.typenames: DISPLAYCONFIG_RATIONAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_RATIONAL
 - wingdi/DISPLAYCONFIG_RATIONAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_RATIONAL
---

# DISPLAYCONFIG_RATIONAL structure


## -description

The DISPLAYCONFIG_RATIONAL structure describes a fractional value that represents vertical and horizontal frequencies of a video mode (that is, vertical sync and horizontal sync).

## -struct-fields

### -field Numerator

The numerator of the frequency fraction.

### -field Denominator

The denominator of the frequency fraction.

## -remarks

A DISPLAYCONFIG_RATIONAL structure is specified in members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> structures.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_video_signal_info">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a>