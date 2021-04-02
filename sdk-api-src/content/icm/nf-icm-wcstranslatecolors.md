---
UID: NF:icm.WcsTranslateColors
title: WcsTranslateColors
description: Translates an array of colors from the source color space to the destination color space as defined by a color transform.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - mscms.dll
api_name:
 - WcsTranslateColors
f1_keywords:
 - WcsTranslateColors
 - icm/WcsTranslateColors
dev_langs:
 - c++
---

## -description

Translates an array of colors from the source color space to the destination color space as defined by a color transform.

## -parameters

### -param hColorTransform

A handle for the WCS color transform.

### -param nColors

The number of elements in the array to which *pInputData* and *pOutputData* point.

### -param nInputChannels

The number of channels per element in the array to which *pInputData* points.

### -param cdtInput

The input [**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype) color data type.

### -param cbInput

The buffer size, in bytes, of *pInputData*.

### -param pInputData

A pointer to an array of input colors. The size of the buffer for this array, in bytes, is the **DWORD** value of *cbInput*.

### -param nOutputChannels

The number of channels per element in the array to which *pOutputData* points.

### -param cdtOutput

The [**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype) output that specified the color data type.

### -param cbOutput

The buffer size, in bytes, of *pOutputData*.

### -param pOutputData

A pointer to an array of colors that receives the results of the color translation.The size of the buffer for this array, in bytes, is the **DWORD** value of *cbOutput*.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the input and the output color data types are not compatible with the color transform, this function fails. This function will fail if an ICC transform is used.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
