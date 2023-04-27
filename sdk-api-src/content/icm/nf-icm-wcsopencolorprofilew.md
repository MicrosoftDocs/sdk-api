---
UID: NF:icm.WcsOpenColorProfileW
title: WcsOpenColorProfileW
description: Creates a handle to a specified color profile. (Unicode)
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
 - WcsOpenColorProfileW
 - WcsOpenColorProfile
f1_keywords:
 - WcsOpenColorProfileW
 - icm/WcsOpenColorProfileW
 - WcsOpenColorProfile
 - icm/WcsOpenColorProfile
dev_langs:
 - c++
---

## -description

Creates a handle to a specified color profile.

## -parameters

### -param pCDMPProfile

Pointer to a WCS DMP or an ICC color profile structure specifying the profile. You can free the *pCDMPProfile* pointer after you create the handle. If the profile is ICC and its **dwType** member is set to DONT\_USE\_EMBEDDED\_WCS\_PROFILES, **WcsOpenColorProfile** ignores any embedded WCS profile within the ICC profile.

### -param pCAMPProfile

A pointer to a profile structure that specifies a WCS color appearance model profile (CAMP). You can free the *pCAMPProfile* pointer after you create the handle. If **NULL**, the default CAMP is used, and the current user setting, WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, is used while querying the default CAMP.

### -param pGMMPProfile

A pointer to a profile structure that specifies a WCS gamut map model profile (GMMP). You can free the *pGMMPProfile* pointer after you create the handle. If **NULL**, the default GMMP for the default rendering intent is used, and the current user setting, WCS\_PROFILE\_MANAGEMENT\_SCOPE\_CURRENT\_USER, is used while querying the default GMMP. For a description of rendering intents, see [Rendering Intents](/windows/win32/wcs/rendering-intents).

### -param dwDesireAccess

A flag value that specifies how to access the specified color profile. This parameter must take one of the following values:

| Value | Description |
|-|-|
| PROFILE\_READ | Specifies that the color profile opens for read-only access. |
| PROFILE\_READWRITE | Specifies that the color profile opens for both read and write access. The value of this flag is ignored if the profile is a WCS profile. |

### -param dwShareMode

A flag value that specifies actions to take while opening a color profile contained in a file. This parameter must take one of the following values, which are defined in *winnt.h*:

| Value | Description |
|-|-|
| FILE\_SHARE\_READ | Specifies that you can perform other open (for read access) operations on the profile. |
| FILE\_SHARE\_WRITE | Specifies that you can perform other open (for write access) operations on the profile. This flag value is ignored when a WCS profile is opened. |

### -param dwCreationMode

A flag value that specifies the actions to take while opening a color profile if it is contained in a file. This parameter must take one of the following values, which are defined in *winbase.h*:

| Value | Description |
|-|-|
| CREATE\_NEW | Specifies that a new profile is created. This function fails if the profile already exists. |
| CREATE\_ALWAYS | Specifies that a new profile is created. If a profile already exists, it is overwritten. |
| OPEN\_EXISTING | Specifies that the profile is opened. This function fails if the profile does not exist. |
| OPEN\_ALWAYS | Specifies that the profile is to be opened if an International Color Consortium (ICC) file exists. If an ICC profile does not exist, WCS creates a new ICC profile. The function will fail for WCS profiles if this flag is set and a WCS profile does not exist. |
| TRUNCATE\_EXISTING | Specifies that the profile is to be opened and truncated to zero bytes. The function fails if the profile does not exist. |

### -param dwFlags

A flag value that specifies whether to use the embedded WCS profile. This parameter has no effect unless *pCDMProfile* specifies an ICC profile that contains an embedded WCS profile.

This parameter takes one of the following values:

| Value | Description |
|-|-|
| 0 | Specifies that the embedded WCS profile will be used and the ICC profile specfied by pCDMPProfile will be ignored. |
| DONT\_USE\_EMBEDDED\_WCS\_PROFILES | Specifies that the ICC profile specified by pCDMPProfile will be used and the embedded WCS profile will be ignored. |

## -returns

If this function succeeds, the return value is the handle of the color profile that is opened.

If this function fails, the return value is **NULL**.

## -remarks

This API will take a set of DMP, CAMP, and GMMP and return a WCS profile handle. **NULL** values for GMMP are valid. A **NULL** value for CAMP will be replaced with the default CAMP value.

This API will also accept ICC profiles. Using an ICC profile does not guarantee processing by the WCS CITE engine. The WCS engine will only be used if it is passed at least one WCS profile. Pure ICC workflows will be consistent with legacy behavior.

You can use the handle that this function returns in other color profile management functions.

The *dwCreationMode* flags CREATE\_NEW, CREATE\_ALWAYS, and TRUNCATE\_EXISTING will always return blank ICC HPROFILEs. If other *dwCreationMode* flags are present, the function will determine whether the profile is ICC or WCS XML.

Within the ICC code path, an ICC HPROFILE is returned using the requested sharing, access, and creation flags as specified in the tables above.

Within the WCS path, the *dwCreationMode* flag OPEN\_ALWAYS will fail if the profile does not exist, because WCS profiles cannot be created or edited within the WCS architecture (they must be edited outside of it, using MSXML6). For the same reason, *dwShareMode* flag FILE\_SHARE\_WRITE, and the *dwDesiredAccess* flag PROFILE\_READWRITE are ignored within the WCS path.

Once the handle to the color profile is created, any information used to create that handle can be deleted.

Use the [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) function to close an object handle that is returned by **WcsOpenColorProfile**.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
* [Functions](/windows/win32/wcs/functions)
