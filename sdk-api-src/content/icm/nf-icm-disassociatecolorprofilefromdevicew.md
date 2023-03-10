---
UID: NF:icm.DisassociateColorProfileFromDeviceW
title: DisassociateColorProfileFromDeviceW
description: Disassociates a specified color profile with a specified device on a specified computer. (Unicode)
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
 - DisassociateColorProfileFromDeviceW
 - DisassociateColorProfileFromDevice
f1_keywords:
 - DisassociateColorProfileFromDeviceW
 - icm/DisassociateColorProfileFromDeviceW
 - DisassociateColorProfileFromDevice
 - icm/DisassociateColorProfileFromDevice
dev_langs:
 - c++
---

## -description

Disassociates a specified color profile with a specified device on a specified computer.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileRemoveDisplayAssociation**](nf-icm-colorprofileremovedisplayassociation.md) for managing advanced color profiles.

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the computer on which to disassociate the specified profile and device. A **NULL** pointer indicates the local computer.

### -param pProfileName

Pointer to the file name of the profile to disassociate.

### -param pDeviceName

Pointer to the name of the device to disassociate.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If more than one profile is associated with a device, WCS uses the last one associated as the default. That is, if your application sequentially associates three profiles with a device, WCS will use the last one associated as the default. If your application then calls the **DisassociateColorProfileFromDevice** function to disassociate the third profile (which is the default in this example), the WCS will use the second profile as the default.

If your application disassociates all profiles from a device, WCS uses the sRGB profile as the default.

**DisassociateColorProfileFromDevice** always removes the specified profile from the current user's per-user profile association list for the specified device. Before removing the profile from the list, **DisassociateColorProfileFromDevice** determines whether the user has previously expressed the desire to use a per-user profile association list for the device. If so, then **DisassociateColorProfileFromDevice** simply removes the specified profile from the existing per-user profile association list for the device. If not, then **DisassociateColorProfileFromDevice** creates a new per-user profile association list for the device by copying the system-wide association list for that device. It then removes the specified profile from the per-user list. From that point on, the current user will be using a per-user profile association list for the specified device, as if [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles) had been called for *pDevice* with the *usePerUserProfiles* parameter set to **TRUE**.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [AssociateColorProfileWithDeviceW](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)
