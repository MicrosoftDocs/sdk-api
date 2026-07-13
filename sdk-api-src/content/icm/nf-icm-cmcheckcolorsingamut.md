---
UID: NF:icm.CMCheckColorsInGamut
title: CMCheckColorsInGamut
description: Determines whether specified RGB triples lie in the output [gamut](/windows/win32/wcs/g) of a specified transform.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
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
 - icm.h
api_name:
 - CMCheckColorsInGamut
f1_keywords:
 - CMCheckColorsInGamut
 - icm/CMCheckColorsInGamut
dev_langs:
 - c++
---

## -description

\[**CMCheckColorsInGamut** is no longer available for use as of Windows Vista.\]

Determines whether specified RGB triples lie in the output [gamut](/windows/win32/wcs/g) of a specified transform.

## -parameters

### -param hcmTransform

Specifies the transform to use.

### -param lpaRGBTriple

Points to an array of RGB triples to check.

### -param lpaResult

Points to the buffer in which to put results.
    
The results are represented by an array of bytes. Each byte in the array corresponds to an RGB triple and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer *n* in the range 0 \< *n* \< 255, a result value of *n* + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of *n*.

### -param nCount

Specifies the number of elements in the array.

## -returns

Beginning with Windows Vista, the default CMM (Icm32.dll) will return **FALSE** and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) will report ERROR\_NOT\_SUPPORTED.

**Windows Server 2003, Windows XP and Windows 2000:**

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. Call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error.

## -remarks

Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

**Windows Server 2003, Windows XP and Windows 2000:**

CMM Implementors are required to implement this method.

Every CMM is required to export this function.

If the function is not successful, custom CMMs should call [SetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) to set the last error to a valid error value defined in Winerror.h.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
