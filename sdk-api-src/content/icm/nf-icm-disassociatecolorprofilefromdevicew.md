---
UID: NF:icm.DisassociateColorProfileFromDeviceW
title: DisassociateColorProfileFromDeviceW function
author: windows-driver-content
description: The DisassociateColorProfileFromDevice function disassociates a specified color profile with a specified device on a specified computer.
old-location: wcs\disassociatecolorprofilefromdevice.htm
old-project: WCS
ms.assetid: 731b4172-3bd6-4f6f-9045-07f36197e120
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DisassociateColorProfileFromDevice, DisassociateColorProfileFromDevice function [Windows Color System], DisassociateColorProfileFromDeviceA, DisassociateColorProfileFromDeviceW, _color_DisassociateColorProfileFromDevice, icm/DisassociateColorProfileFromDevice, icm/DisassociateColorProfileFromDeviceA, icm/DisassociateColorProfileFromDeviceW, wcs.disassociatecolorprofilefromdevice
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
req.unicode-ansi: DisassociateColorProfileFromDeviceW (Unicode) and DisassociateColorProfileFromDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	DisassociateColorProfileFromDevice
-	DisassociateColorProfileFromDeviceA
-	DisassociateColorProfileFromDeviceW
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# DisassociateColorProfileFromDeviceW function


## -description


The <b>DisassociateColorProfileFromDevice</b> function disassociates a specified color profile with a specified device on a specified computer.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the computer on which to disassociate the specified profile and device. A <b>NULL</b> pointer indicates the local computer.


### -param pProfileName

Pointer to the file name of the profile to disassociate.


### -param pDeviceName

Pointer to the name of the device to disassociate.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If more than one profile is associated with a device, WCS uses the last one associated as the default. That is, if your application sequentially associates three profiles with a device, WCS will use the last one associated as the default. If your application then calls the <b>DisassociateColorProfileFromDevice</b> function to disassociate the third profile (which is the default in this example), the WCS will use the second profile as the default.

If your application disassociates all profiles from a device, WCS uses the sRGB profile as the default.

<b>DisassociateColorProfileFromDevice</b> always removes the specified profile from the current user's per-user profile association list for the specified device. Before removing the profile from the list, <b>DisassociateColorProfileFromDevice</b> determines whether the user has previously expressed the desire to use a per-user profile association list for the device. If so, then <b>DisassociateColorProfileFromDevice</b> simply removes the specified profile from the existing per-user profile association list for the device. If not, then <b>DisassociateColorProfileFromDevice</b> creates a new per-user profile association list for the device by copying the system-wide association list for that device. It then removes the specified profile from the per-user list. From that point on, the current user will be using a per-user profile association list for the specified device, as if <a href="https://msdn.microsoft.com/library/windows/hardware/ff563741">WcsSetUsePerUserProfiles</a> had been called for <i>pDevice</i> with the <i>usePerUserProfiles</i> parameter set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/2a4adfde-ab91-48f1-8212-3263006ea3a1">AssociateColorProfileWithDevice</a>



<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

