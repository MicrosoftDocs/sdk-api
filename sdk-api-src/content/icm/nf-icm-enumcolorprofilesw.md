---
UID: NF:icm.EnumColorProfilesW
title: EnumColorProfilesW
description: Enumerates all the profiles satisfying the given enumeration criteria. (Unicode)
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
req.lib: Mscms.Lib
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
 - EnumColorProfilesW
 - EnumColorProfiles
f1_keywords:
 - EnumColorProfilesW
 - icm/EnumColorProfilesW
 - EnumColorProfiles
 - icm/EnumColorProfiles
dev_langs:
 - c++
---

## -description

Enumerates all the profiles satisfying the given enumeration criteria.

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the computer on which to enumerate profiles. A **NULL** pointer indicates the local computer.

### -param pEnumRecord

Pointer to a structure specifying the enumeration criteria.

### -param pEnumerationBuffer

Pointer to a buffer in which the profiles are to be enumerated. A MULTI\_SZ string of profile names satisfying the criteria specified in *\*pEnumRecord* will be placed in this buffer.

### -param pdwSizeOfEnumerationBuffer

Pointer to a variable containing the size of the buffer pointed to by *pBuffer*. On return, *\*pdwSize* contains the size of buffer actually used or needed.

### -param pnProfiles

Pointer to a variable that will contain, on return, the number of profile names actually copied to the buffer.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Several profiles are typically associated with printers, based on the paper and ink types. There is a default profile for each device. For International Color Consortium (ICC) profiles, GDI selects the best one from the ICC-associated profiles when your application creates a device context (DC).

Do not attempt to use **EnumColorProfiles** to determine the default profile for a device. Instead, create a device context for the device and then invoke the [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea) function. On Windows Vista and Windows 7, the [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) function can also be used to determine a device's default color profile.

If the **dwFields** member of the structure of type **ENUMTYPE** that is pointed to by the *pEnumRecord* parameter is set to ET\_DEVICENAME, this function will enumerate all of the color profiles associated with all types of devices attached to the user's computer, regardless of the device class. If the **dwFields** member of the structure pointed to by the *pEnumRecord* parameter is set to ET\_DEVICENAME or ET\_DEVICECLASS and a device class is specified in the **dwDeviceClass** member of the structure, this function will only enumerate the profiles associated with the specified device class. If the **dwFields** member is set only to ET\_DEVICECLASS, the **EnumColorProfiles** function will enumerate all profiles that can be associated with that type of device.

Whenever **EnumColorProfiles** is examining the profiles associated with a specific device, the results depend on whether the user has chosen to use the system-wide list of profiles associated with that device, or his or her own ("per-user") list. Calling [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles) with its *usePerUserProfiles* parameter set to **TRUE** causes future calls to **EnumColorProfiles** to look at only the current user's per-user list of profile associations for the specified device. Calling **WcsSetUsePerUserProfiles** with its *usePerUserProfiles* parameter set to **FALSE** causes future calls to **EnumColorProfiles** to look at the system-wide list of profile associations for the specified device. If **WcsSetUsePerUserProfiles** has never been called for the current user, **EnumColorProfiles** examines the system-wide list.

Your application can use **EnumColorProfiles** to obtain the size of the buffer in which the profiles are enumerated. It should call the **EnumColorProfiles** function with the *pBuffer* parameter set to **NULL**. When the function returns, the *pdwSize* parameter will contain the required buffer size in bytes. Your program can use that information to allocate the enumeration buffer. It can then invoke **EnumColorProfiles** again with the *pBuffer* parameter set to the address of the buffer.

This function will provide the information for converting WCS-specific DMP information to the legacy EnumType record in enable consistent profile enumeration. The defaults will be the same as ICC if this information is not present.

### Per-user/LUA support

The enumeration is specific to current user. Both system wide and current user device associations are considered. For default profile configuration, current user settings override system wide ones.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [GetICMProfile](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)
* [ENUMTYPEW](/windows/win32/api/icm/ns-icm-enumtypew)
