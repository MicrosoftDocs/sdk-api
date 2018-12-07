---
UID: NF:icm.AssociateColorProfileWithDeviceA
title: AssociateColorProfileWithDeviceA function
author: windows-sdk-content
description: The AssociateColorProfileWithDevice function associates a specified color profile with a specified device.
old-location: wcs\associatecolorprofilewithdevice.htm
tech.root: WCS
ms.assetid: 2a4adfde-ab91-48f1-8212-3263006ea3a1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AssociateColorProfileWithDevice, AssociateColorProfileWithDevice function [Windows Color System], AssociateColorProfileWithDeviceA, AssociateColorProfileWithDeviceW, _color_AssociateColorProfileWithDevice, icm/AssociateColorProfileWithDevice, icm/AssociateColorProfileWithDeviceA, icm/AssociateColorProfileWithDeviceW, wcs.associatecolorprofilewithdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AssociateColorProfileWithDeviceW (Unicode) and AssociateColorProfileWithDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - AssociateColorProfileWithDevice
 - AssociateColorProfileWithDeviceA
 - AssociateColorProfileWithDeviceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- AssociateColorProfileWithDeviceA
: 
---

# AssociateColorProfileWithDeviceA function


## -description


The <b>AssociateColorProfileWithDevice</b> function associates a specified color profile with a specified device.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the machine on which to associate the specified profile and device. A <b>NULL</b> pointer indicates the local machine.


### -param pProfileName

Points to the file name of the profile to associate.


### -param pDeviceName

Points to the name of the device to associate.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>AssociateColorProfileWithDevice</b> function will fail if the profile has not been installed on the computer using the <a href="https://msdn.microsoft.com/494b2080-a0a8-4fda-bc12-3bf196a6840c">InstallColorProfile</a> function.

Note that under Windows (Windows 95 or later), the PostScript device driver for printers assumes a CMYK color model. Therefore, all PostScript printers must use a CMYK color profile. Windows 2000 does not have this limitation.

If the specified device is a monitor, this function updates the default profile.

Several profiles are typically associated with printers, based on paper and ink types. There is no default. The GDI selects the best one from the associated profiles when your application creates a device context (DC).

Scanners also have no default profile. However, it is atypical to associate more than one profile with a scanner.

<b>AssociateColorProfileWithDevice</b> always adds the specified profile to the current user's per-user profile association list for the specified device. Before adding the profile to the list, <b>AssociateColorProfileWithDevice</b> determines whether the user has previously expressed the desire to use a per-user profile association list for the device. If so, then <b>AssociateColorProfileWithDevice</b> simply adds the specified profile to the existing per-user profile association list for the device. If not, then <b>AssociateColorProfileWithDevice</b> creates a new per-user profile association list for the device by copying the system-wide association list for that device. It then appends the specified profile to the per-user list. From that point on, the current user will be using a per-user profile association list for the specified device, as if <a href="https://msdn.microsoft.com/c108fbb2-e9f3-41fe-af36-99114df1507e">WcsSetUsePerUserProfiles</a> had been called for <i>pDevice</i> with the <i>usePerUserProfiles</i> parameter set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/731b4172-3bd6-4f6f-9045-07f36197e120">DisassociateColorProfileFromDevice</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

