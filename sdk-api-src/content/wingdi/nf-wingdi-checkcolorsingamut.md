---
UID: NF:wingdi.CheckColorsInGamut
title: CheckColorsInGamut function (wingdi.h)
description: The CheckColorsInGamut function determines whether a specified set of RGB triples lies in the output gamut of a specified device. The RGB triples are interpreted in the input logical color space.
helpviewer_keywords: ["CheckColorsInGamut","CheckColorsInGamut function [Windows Color System]","_color_CheckColorsInGamut","wcs.checkcolorsingamut","wingdi/CheckColorsInGamut"]
old-location: wcs\checkcolorsingamut.htm
tech.root: WCS
ms.assetid: 87bee1a6-e3dd-4d0b-ad8a-9584833d9463
ms.date: 12/05/2018
ms.keywords: CheckColorsInGamut, CheckColorsInGamut function [Windows Color System], _color_CheckColorsInGamut, wcs.checkcolorsingamut, wingdi/CheckColorsInGamut
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CheckColorsInGamut
 - wingdi/CheckColorsInGamut
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CheckColorsInGamut
---

# CheckColorsInGamut function


## -description

The <b>CheckColorsInGamut</b> function determines whether a specified set of RGB triples lies in the output [gamut](/windows/win32/wcs/g) of a specified device. The RGB triples are interpreted in the input logical color space.

## -parameters

### -param hdc

Handle to the device context whose output gamut to be checked.

### -param lpRGBTriple

Pointer to an array of RGB triples to check.

### -param dlpBuffer

Pointer to the buffer in which the results are to be placed. This buffer must be at least as large as <i>nCount</i> bytes.

### -param nCount

The number of elements in the array of triples.

## -returns

If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero.

## -remarks

The function places the test results in the buffer pointed to by <i>lpBuffer</i>. Each byte in the buffer corresponds to an <i>RGB triple</i>, and has an unsigned value between CM_IN_GAMUT (= 0) and CM_OUT_OF_GAMUT (= 255). The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> such that 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>, as specified by the ICC Profile Format Specification. For more information on the ICC Profile Format Specification, see the sources listed in [Further information](/windows/win32/wcs/further-information)
.

Note that for this function to succeed, WCS must be enabled for the device context handle that is passed in through the <i>hDC</i> parameter. WCS can be enabled for a device context handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmmode">SetICMMode</a> function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [SetICMMode](/windows/win32/api/wingdi/nf-wingdi-seticmmode)
