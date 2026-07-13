---
UID: NF:icm.AssociateColorProfileWithDeviceA
title: AssociateColorProfileWithDeviceA
description: Associates a specified color profile with a specified device. (ANSI)
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - AssociateColorProfileWithDeviceA
 - AssociateColorProfileWithDevice
f1_keywords:
 - AssociateColorProfileWithDeviceA
 - icm/AssociateColorProfileWithDeviceA
 - AssociateColorProfileWithDevice
 - icm/AssociateColorProfileWithDevice
dev_langs:
 - c++
---

## -description

Associates a specified color profile with a specified device.

> [!NOTE] 
> This API does not support "advanced color" profiles for HDR monitors. Use [**ColorProfileAddDisplayAssociation**](nf-icm-colorprofileadddisplayassociation.md) for managing advanced color profiles.

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the machine on which to associate the specified profile and device. A **NULL** pointer indicates the local machine.

### -param pProfileName

Points to the file name of the profile to associate.

### -param pDeviceName

Points to the name of the device to associate.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The **AssociateColorProfileWithDevice** function will fail if the profile has not been installed on the computer using the [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) function.

Note that under Windows (Windows 95 or later), the PostScript device driver for printers assumes a CMYK color model. Therefore, all PostScript printers must use a CMYK color profile. Windows 2000 does not have this limitation.

If the specified device is a monitor, this function updates the default profile.

Several profiles are typically associated with printers, based on paper and ink types. There is no default. The GDI selects the best one from the associated profiles when your application creates a device context (DC).

Scanners also have no default profile. However, it is atypical to associate more than one profile with a scanner.

**AssociateColorProfileWithDevice** always adds the specified profile to the current user's per-user profile association list for the specified device. Before adding the profile to the list, **AssociateColorProfileWithDevice** determines whether the user has previously expressed the desire to use a per-user profile association list for the device. If so, then **AssociateColorProfileWithDevice** simply adds the specified profile to the existing per-user profile association list for the device. If not, then **AssociateColorProfileWithDevice** creates a new per-user profile association list for the device by copying the system-wide association list for that device. It then appends the specified profile to the per-user list. From that point on, the current user will be using a per-user profile association list for the specified device, as if [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles) had been called for *pDevice* with the *usePerUserProfiles* parameter set to **TRUE**.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [DisassociateColorProfileFromDevice](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew)
