---
UID: NF:icm.WcsCheckColors
title: WcsCheckColors
description: Determines whether the colors in an array are within the output gamut of a specified WCS color transform.
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
 - WcsCheckColors
f1_keywords:
 - WcsCheckColors
 - icm/WcsCheckColors
dev_langs:
 - c++
---

## -description

Determines whether the colors in an array are within the output gamut of a specified WCS color transform.

## -parameters

### -param hColorTransform

A handle to the specified WCS color transform.

### -param nColors

The number of elements in the array pointed to by *pInputData* and *paResult*.

### -param nInputChannels

The number of channels per element in the array pointed to by *pInputData*.

### -param cdtInput

The input COLORDATATYPE color data type.

### -param cbInput

The buffer size of *pInputData*.

### -param pInputData

A pointer to an array of input colors. Colors in this array correspond to the color space of the source profile. The size of the buffer for this array will be the number of bytes indicated by *cbInput*.

### -param paResult

A pointer to an array of *nColors* bytes that receives the results of the test.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the input and the output color data types are not compatible with the color transform, this function will convert the input color data as required.

This function fails if you use an International Color Consortium (ICC) transform is used.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
