---
UID: NS:wingdi._DISPLAYCONFIG_SDR_WHITE_LEVEL
tech.root: 
title: DISPLAYCONFIG_SDR_WHITE_LEVEL
ms.date: 08/08/2022
targetos: Windows
description: The DISPLAYCONFIG_SDR_WHITE_LEVEL structure (wingdi.h) contains information about a display's current SDR white level.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wingdi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DISPLAYCONFIG_SDR_WHITE_LEVEL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - _DISPLAYCONFIG_SDR_WHITE_LEVEL
 - DISPLAYCONFIG_SDR_WHITE_LEVEL
f1_keywords:
 - _DISPLAYCONFIG_SDR_WHITE_LEVEL
 - wingdi/_DISPLAYCONFIG_SDR_WHITE_LEVEL
 - DISPLAYCONFIG_SDR_WHITE_LEVEL
 - wingdi/DISPLAYCONFIG_SDR_WHITE_LEVEL
dev_langs:
 - c++
---

## -description

The __DISPLAYCONFIG_SDR_WHITE_LEVEL__ structure contains information about a display's current SDR white level. This is the brightness level that SDR "white" is rendered at within an HDR monitor.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information for getting the SDR white level. The <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER is set to DISPLAYCONFIG_DEVICE_INFO_GET_SDR_WHITE_LEVEL. DISPLAYCONFIG_DEVICE_INFO_HEADER also contains the adapter and target identifiers of the target to get the SDR white level for. The <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER is set to at least the size of the DISPLAYCONFIG_SDR_WHITE_LEVEL structure.

### -field SDRWhiteLevel

The monitor's current SDR white level, specified as a multiplier of 80 nits, multiplied by 1000. E.g. a value of 1000 would indicate that the SDR white level is 80 nits, while a value of 2000 would indicate an SDR white level of 160 nits.

```cpp
DISPLAYCONFIG_SDR_WHITE_LEVEL sdrWhiteLevel;
...
float SDRWhiteLevelInNits = (float)sdrWhiteLevel.SDRWhiteLevel / 1000 * 80;
```

## -remarks

## -see-also

[Using DirectX with high dynamic range Displays and Advanced Color
](/windows/win32/direct3darticles/high-dynamic-range)

[DISPLAYCONFIG_DEVICE_INFO_HEADER](ns-wingdi-displayconfig_device_info_header.md)

[DisplayConfigGetDeviceInfo](../winuser/nf-winuser-displayconfiggetdeviceinfo.md)
