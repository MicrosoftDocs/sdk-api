---
UID: NC:wingdi.ICMENUMPROCW
title: ICMENUMPROCW (wingdi.h)
description: The EnumICMProfilesProcCallback callback is an application-defined callback function that processes color profile data from EnumICMProfiles . (Unicode)
helpviewer_keywords: ["ICMENUMPROC","ICMENUMPROC callback","ICMENUMPROC callback function [Windows Color System]","ICMENUMPROCA","ICMENUMPROCW","_color_EnumICMProfilesProcCallback","wcs.enumicmprofilesproccallback","wingdi/ICMENUMPROC","wingdi/ICMENUMPROCA","wingdi/ICMENUMPROCW"]
old-location: wcs\enumicmprofilesproccallback.htm
tech.root: WCS
ms.assetid: 6e8f4ce5-c546-4e6a-8f35-4a22d60b6754
ms.date: 12/05/2018
ms.keywords: ICMENUMPROC, ICMENUMPROC callback, ICMENUMPROC callback function [Windows Color System], ICMENUMPROCA, ICMENUMPROCW, _color_EnumICMProfilesProcCallback, wcs.enumicmprofilesproccallback, wingdi/ICMENUMPROC, wingdi/ICMENUMPROCA, wingdi/ICMENUMPROCW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ICMENUMPROCW (Unicode) and ICMENUMPROCA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICMENUMPROCW
 - wingdi/ICMENUMPROCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - ICMENUMPROC
 - ICMENUMPROCA
 - ICMENUMPROCW
---

# ICMENUMPROCW callback function


## -description

The <b>EnumICMProfilesProcCallback</b> callback is an application-defined callback function that processes color profile data from <b>EnumICMProfiles</b> .

## -parameters

### -param unnamedParam1

### -param unnamedParam2

#### - lParam

Data supplied by the application that is passed to the callback function by the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumicmprofilesa">EnumICMProfiles</a> function.


#### - lpszFilename

Pointer to the file name of the color profile.

## -returns

This function must return a positive value to continue enumeration, or zero to stop enumeration. It may not return a negative value.

## -remarks

> [!NOTE]
> The wingdi.h header defines ICMENUMPROC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [EnumICMProfilesW](/windows/win32/api/wingdi/nf-wingdi-enumicmprofilesw)
