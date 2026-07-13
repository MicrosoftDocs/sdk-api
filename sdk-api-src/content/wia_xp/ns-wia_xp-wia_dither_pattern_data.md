---
UID: NS:wia_xp._WIA_DITHER_PATTERN_DATA
title: WIA_DITHER_PATTERN_DATA (wia_xp.h)
description: The WIA_DITHER_PATTERN_DATA structure specifies a dither pattern for scanners. It is used in conjunction with the scanner device property constant WIA_DPS_DITHER_PATTERN_DATA.
helpviewer_keywords: ["*PWIA_DITHER_PATTERN_DATA","PWIA_DITHER_PATTERN_DATA","PWIA_DITHER_PATTERN_DATA structure pointer [WIA]","WIA_DITHER_PATTERN_DATA","WIA_DITHER_PATTERN_DATA structure [WIA]","_wia_WIA_DITHER_PATTERN_DATA","wia._wia_WIA_DITHER_PATTERN_DATA","wia_xp/PWIA_DITHER_PATTERN_DATA","wia_xp/WIA_DITHER_PATTERN_DATA"]
old-location: wia\_wia_WIA_DITHER_PATTERN_DATA.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\structs\wia_dither_pattern_data.htm
ms.date: 12/05/2018
ms.keywords: '*PWIA_DITHER_PATTERN_DATA, PWIA_DITHER_PATTERN_DATA, PWIA_DITHER_PATTERN_DATA structure pointer [WIA], WIA_DITHER_PATTERN_DATA, WIA_DITHER_PATTERN_DATA structure [WIA], _wia_WIA_DITHER_PATTERN_DATA, wia._wia_WIA_DITHER_PATTERN_DATA, wia_xp/PWIA_DITHER_PATTERN_DATA, wia_xp/WIA_DITHER_PATTERN_DATA'
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WIA_DITHER_PATTERN_DATA, *PWIA_DITHER_PATTERN_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WIA_DITHER_PATTERN_DATA
 - wia_xp/_WIA_DITHER_PATTERN_DATA
 - PWIA_DITHER_PATTERN_DATA
 - wia_xp/PWIA_DITHER_PATTERN_DATA
 - WIA_DITHER_PATTERN_DATA
 - wia_xp/WIA_DITHER_PATTERN_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wia_xp.h
api_name:
 - WIA_DITHER_PATTERN_DATA
archived: true
---

# WIA_DITHER_PATTERN_DATA structure


## -description

The <b>WIA_DITHER_PATTERN_DATA</b> structure specifies a dither pattern for scanners. It is used in conjunction with the <a href="/windows/desktop/wia/-wia-wiaitempropscannerdevice">scanner device property constant</a> WIA_DPS_DITHER_PATTERN_DATA.

## -struct-fields

### -field lSize

Type: <b>LONG</b>

Specifies the size of this structure in bytes. Should be set to <b>sizeof(WIA_DITHER_PATTERN_DATA)</b>.

### -field bstrPatternName

Type: <b>BSTR</b>

Specifies a string that contains the name of this dither pattern.

### -field lPatternWidth

Type: <b>LONG</b>

Indicates the width of the dither pattern in bytes.

### -field lPatternLength

Type: <b>LONG</b>

Indicates the length of the dither pattern in bytes.

### -field cbPattern

Type: <b>LONG</b>

Specifies the total number of bytes in the array pointed to by the <b>pbPattern</b> member.

### -field pbPattern

Type: <b>BYTE*</b>

Specifies a pointer to a buffer that contains the dither pattern.