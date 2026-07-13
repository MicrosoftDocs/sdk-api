---
UID: NF:vfw.capGetDriverDescriptionA
title: capGetDriverDescriptionA function (vfw.h)
description: The capGetDriverDescription function retrieves the version description of the capture driver. (ANSI)
helpviewer_keywords: ["capGetDriverDescriptionA", "vfw/capGetDriverDescriptionA"]
old-location: multimedia\capgetdriverdescription.htm
tech.root: Multimedia
ms.assetid: 97ec77f8-79fe-4c0b-9b73-5b09903c47b2
ms.date: 12/05/2018
ms.keywords: _win32_capGetDriverDescription, capGetDriverDescription, capGetDriverDescription function [Windows Multimedia], capGetDriverDescriptionA, capGetDriverDescriptionW, multimedia.capgetdriverdescription, vfw/capGetDriverDescription, vfw/capGetDriverDescriptionA, vfw/capGetDriverDescriptionW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: capGetDriverDescriptionW (Unicode) and capGetDriverDescriptionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avicap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - capGetDriverDescriptionA
 - vfw/capGetDriverDescriptionA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avicap32.dll
api_name:
 - capGetDriverDescription
 - capGetDriverDescriptionA
 - capGetDriverDescriptionW
---

# capGetDriverDescriptionA function


## -description

The <b>capGetDriverDescription</b> function retrieves the version description of the capture driver.

## -parameters

### -param wDriverIndex

Index of the capture driver. The index can range from 0 through 9.

Plug-and-Play capture drivers are enumerated first, followed by capture drivers listed in the registry, which are then followed by capture drivers listed in SYSTEM.INI.

### -param lpszName

Pointer to a buffer containing a null-terminated string corresponding to the capture driver name.

### -param cbName

Length, in bytes, of the buffer pointed to by <i>lpszName</i>.

### -param lpszVer

Pointer to a buffer containing a null-terminated string corresponding to the description of the capture driver.

### -param cbVer

Length, in bytes, of the buffer pointed to by <i>lpszVer</i>.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

If the information description is longer than its buffer, the description is truncated. The returned string is always null-terminated. If a buffer size is zero, its corresponding description is not copied.





> [!NOTE]
> The vfw.h header defines capGetDriverDescription as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>
