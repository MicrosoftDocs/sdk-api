---
UID: NF:icm.OpenColorProfileW
title: OpenColorProfileW
description: Creates a handle to a specified color profile. The handle can then be used in other profile management functions. (Unicode)
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
 - OpenColorProfileW
 - OpenColorProfile
f1_keywords:
 - OpenColorProfileW
 - icm/OpenColorProfileW
 - OpenColorProfile
 - icm/OpenColorProfile
dev_langs:
 - c++
---

## -description

Creates a handle to a specified color profile. The handle can then be used in other profile management functions.

## -parameters

### -param pProfile

Pointer to a color profile structure specifying the profile. The *pProfile* pointer can be freed as soon as the handle is created.

### -param dwDesiredAccess

Specifies how to access the given profile. This parameter must take one the following constant values.

| Value | Meaning |
|-|-|
| <span id="PROFILE_READ"></span><span id="profile_read"></span><dl> <dt>**PROFILE\_READ**</dt> </dl> | Opens the profile for read access.<br/> |
| <span id="PROFILE_READWRITE"></span><span id="profile_readwrite"></span><dl> <dt>**PROFILE\_READWRITE**</dt> </dl> | Opens the profile for both read and write access. Has no effect for WCS XML profiles.<br/> |

### -param dwShareMode

Specifies how the profile should be shared, if the profile is contained in a file. A value of zero prevents the profile from being shared at all. The parameter can contain one or both of the following constants (combined by addition or logical OR).

| Value | Meaning |
|-|-|
| <span id="FILE_SHARE_READ"></span><span id="file_share_read"></span><dl> <dt>**FILE\_SHARE\_READ**</dt> </dl> | Other open operations can be performed on the profile for read access.<br/> |
| <span id="FILE_SHARE_WRITE"></span><span id="file_share_write"></span><dl> <dt>**FILE\_SHARE\_WRITE**</dt> </dl> | Other open operations can be performed on the profile for write access. Has no effect for WCS XML profiles.<br/> |

### -param dwCreationMode

Specifies which actions to take on the profile while opening it, if it is contained in a file. This parameter must take one of the following constant values.

| Value | Meaning |
|-|-|
| <span id="CREATE_NEW"></span><span id="create_new"></span><dl> <dt>**CREATE\_NEW**</dt> </dl> | Creates a new profile. Fails if the profile already exists.<br/> |
| <span id="CREATE_ALWAYS"></span><span id="create_always"></span><dl> <dt>**CREATE\_ALWAYS**</dt> </dl> | Creates a new profile. Overwrites the profile if it exists.<br/> |
| <span id="OPEN_EXISTING"></span><span id="open_existing"></span><dl> <dt>**OPEN\_EXISTING**</dt> </dl> | Opens the profile. Fails if it does not exist<br/> |
| <span id="OPEN_ALWAYS"></span><span id="open_always"></span><dl> <dt>**OPEN\_ALWAYS**</dt> </dl> | Opens the profile if it exists. For ICC profiles, if the profile does not exist, creates the profile. For WCS XML profiles, if the profile does not exist, returns an error.<br/> |
| <span id="TRUNCATE_EXISTING"></span><span id="truncate_existing"></span><dl> <dt>**TRUNCATE\_EXISTING**</dt> </dl> | Opens the profile, and truncates it to zero bytes, returning a blank ICC profile. Fails if the profile doesn't exist.<br/> |

## -returns

If this function succeeds, the return value is the handle of the color profile that is opened. For ICC and WCS profiles, a CAMP and GMMP are provided by the function based on the current default CAMP and GMMP in the registry.

When OpenColorProfile encounters an ICC profile with an embedded WCS profile, and if the dwType member within the Profile structure does not take the value DONT\_USE\_EMBEDDED\_WCS\_PROFILES, it should extract and use the WCS profile(s) contained in this WcsProfilesTag. The HPROFILE returned would be a WCS HPROFILE.

If this function fails, the return value is **NULL**. For extended error information, call **GetLastError**.

## -remarks

If the profile data is not specified using a file name, *dwShareMode* and *dwCreationMode* are ignored.

*dwCreationMode* flags CREATE\_NEW, CREATE\_ALWAYS, and TRUNCATE\_EXISTING, will always return blank ICC HPROFILEs. If other *dwCreationMode* flags are present, InternalOpenColorProfile is called (using the flags as provided by the API) to determine whether the profile is ICC or WCS XML.

Within the ICC code path, an ICC HPROFILE is returned using the requested sharing, access and creation flags as specified in the tables above.

Within the WCS path, the *dwCreationMode* flag OPEN\_ALWAYS will fail if the profile doesn't exist, since WCS profiles cannot be created or edited within the WCS architecture (they must be edited outside of it, using MSXML6). For the same reason, *dwShareMode* flag FILE\_SHARE\_WRITE, and *dwDesiredAccess* flag PROFILE\_READWRITE are ignored within the WCS path.

When the function opens the ICC profile, it will look for a *WcsProfilesTag* and, if there is one, it will extract and use the original WCS profiles contained therein. (See [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile).)

An HPROFILE with WCS profile information is derived from a DMP by acquiring the default CAMP and default GMMP from the registry. An HPROFILE is a composition of a DMP, CAMP and GMMP.

Once the handle to the color profile is created, any information used to create that handle can be deleted.

Use the [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) function to close an object handle returned by **OpenColorProfile**.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CloseColorProfile](/windows/win32/api/icm/nf-icm-closecolorprofile)
* [PROFILE](/windows/win32/api/icm/ns-icm-profile)
