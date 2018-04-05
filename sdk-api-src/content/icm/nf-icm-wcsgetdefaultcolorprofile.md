---
UID: NF:icm.WcsGetDefaultColorProfile
title: WcsGetDefaultColorProfile function
author: windows-driver-content
description: Retrieves the default color profile for a device, or for a device-independent default if the device is not specified.
old-location: wcs\wcsgetdefaultcolorprofile.htm
old-project: WCS
ms.assetid: a40ea9f3-ec56-459e-a55d-aad1b60ae7d4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WcsGetDefaultColorProfile, WcsGetDefaultColorProfile function [Windows Color System], _color_WcsGetDefaultColorProfile, icm/WcsGetDefaultColorProfile, wcs.wcsgetdefaultcolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
-	WcsGetDefaultColorProfile
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# WcsGetDefaultColorProfile function


## -description


Retrieves the default color profile for a device, or for a device-independent default if the device is not specified.


## -parameters




### -param scope

TBD


### -param pDeviceName [in, optional]

A pointer to the name of the device for which the default color profile is obtained. If <b>NULL</b>, a device-independent default profile is obtained.


### -param cptColorProfileType [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff546018">COLORPROFILETYPE</a> value specifying the color profile type.


### -param cpstColorProfileSubType [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff546012">COLORPROFILESUBTYPE</a> value specifying the color profile subtype.


### -param dwProfileID [in]

The ID of the color space that the color profile represents.


### -param cbProfileName [in]

The buffer size, in bytes, of the buffer that is pointed to by <i>pProfileName</i>.


### -param pProfileName [out]

A pointer to a buffer to receive the name of the color profile. The size of the buffer, in bytes, will be the indicated by <i>cbProfileName</i>. 


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff563752">WCS_PROFILE_MANAGEMENT_SCOPE</a> value specifying the scope of this profile management operation.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563730">WcsGetDefaultColorProfileSize</a> function to obtain the required size of the buffer that is pointed to by the <i>pProfileName</i> parameter.

If WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER is present, it overrides the system-wide default for <i>profileManagementScope</i>.

This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546012">COLORPROFILESUBTYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546018">COLORPROFILETYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563752">WCS_PROFILE_MANAGEMENT_SCOPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563730">WcsGetDefaultColorProfileSize</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

