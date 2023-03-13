---
UID: NF:icm.CreateColorTransformA
title: CreateColorTransformA
description: Creates a color transform that applications can use to perform color management. (ANSI)
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
 - Mscms.dll
api_name:
 - CreateColorTransformA
 - CreateColorTransform
f1_keywords:
 - CreateColorTransformA
 - icm/CreateColorTransformA
 - CreateColorTransform
 - icm/CreateColorTransform
dev_langs:
 - c++
---

## -description

Creates a color transform that applications can use to perform color management.

## -parameters

### -param pLogColorSpace

Pointer to the input [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea).

### -param hDestProfile

Handle to the profile of the destination device. The function determines whether the HPROFILE contains International Color Consortium (ICC) or Windows Color System (WCS) profile information.

### -param hTargetProfile

Handle to the profile of the target device. The function determines whether the HPROFILE contains ICC or WCS profile information.

### -param dwFlags

Specifies flags to used control creation of the transform. See Remarks.

## -returns

If this function succeeds, the return value is a handle to the color transform.

If this function fails, the return value is **NULL**. For extended error information, call **GetLastError**.

## -remarks

If the target profile is **NULL**, the transform goes from the source logical color space to the destination profile. If the target profile is given, the transform goes from the source logical color space to the target profile and then to the destination profile. This allows previewing output meant for the target device on the destination device.

The values in *dwFlags* are intended as hints only. The color management module must determine the best way to use them.

**Windows Vista**: Three new flags have been added that can be used with *dwFlags*:

| Flag | Description |
|-|-|
| **PRESERVEBLACK** | If this bit is set, the transform engine inserts the appropriate black generation GMMP as the last GMMP in the transform sequence. This flag only works in a pure WCS transform. |
| **SEQUENTIAL\_TRANSFORM** | If this bit is set, each step in the WCS processing pipeline is performed for every pixel in the image and no optimized color transform is built. This flag only works in a pure WCS transform.**Restrictions**: A transform created with the SEQUENTIAL\_TRANSFORM flag set may only be used in the thread on which it was created and only for one color translation call at a time. COM must be initialized prior to creating the sequential transform and must remain initialized for the lifetime of the transform object.<br/> |
| **WCS\_ALWAYS** | If this bit is set, even all-ICC transforms will use the WCS code path. |

> [!Note] 
> **SEQUENTIAL\_TRANSFORM** was inadvertently omitted from the icm.h header in the Windows Vista SDK. If you wish to use the **SEQUENTIAL\_TRANSFORM** flag, define it in your application as follows:\#define SEQUENTIAL\_TRANSFORM 0x80800000

For details, see [CMM Transform Creation Flags](/windows/win32/wcs/cmm-transform-creation-flags). All of the flags mentioned there are supported for all types of transforms, except for FAST\_TRANSLATE, which only works in a pure ICC-to-ICC transform.

The **CreateColorTransform** function is used outside of a device context. Colors may shift when transforming from a color profile to the same color profile. This is due to precision errors. Therefore, a color transform should not be performed under these circumstances.

The B2Ax tags are required for any profile that is the target of a transform.

WCS transform support for ICC ColorSpace profiles is limited to RGB colorspace profiles. The following ICC profile types cannot be used in a CITE-processed transform, either a mixed WCS/ICC transform or an all-ICC transform with **WCS\_ALWAYS** set:

- Non-RGB ColorSpace profiles
- NamedColor profiles
- n-channel profiles (where n &gt; 8)
- DeviceLink profiles
- Abstract profiles

## -see-also

- [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
- [Functions](/windows/win32/wcs/functions)
