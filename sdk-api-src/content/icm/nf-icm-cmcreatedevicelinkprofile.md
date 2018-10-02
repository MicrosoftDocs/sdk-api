---
UID: NF:icm.CMCreateDeviceLinkProfile
title: CMCreateDeviceLinkProfile function
author: windows-sdk-content
description: The CMCreateDeviceLinkProfile function creates a device link profile in the format specified by the International Color Consortium in its ICC Profile Format Specification.
old-location: wcs\cmcreatedevicelinkprofile.htm
tech.root: WCS
ms.assetid: 54f46d2c-ddcb-4597-9816-172e507a7fa2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CMCreateDeviceLinkProfile, CMCreateDeviceLinkProfile function [Windows Color System], _color_CMCreateDeviceLinkProfile, icm/CMCreateDeviceLinkProfile, wcs.cmcreatedevicelinkprofile
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMCreateDeviceLinkProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMCreateDeviceLinkProfile function


## -description


The <b>CMCreateDeviceLinkProfile</b> function creates a <a href="d.htm">device link profile</a> in the format specified by the International Color Consortium in its ICC Profile Format Specification.


## -parameters




### -param pahProfiles

TBD


### -param nProfiles

Specifies the number of profiles in the array.


### -param padwIntents

An array of rendering intents.


### -param nIntents

The number of elements in the array of intents.


### -param dwFlags

Specifies flags to used control creation of the transform. For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>.


### -param lpProfileData

Pointer to a pointer to a buffer. If successful the function allocates and fills this buffer. The calling application must free this buffer when it is no longer needed. Use the <b>GlobalFree</b> function to free this buffer.


#### - lpahProfiles

Pointer to an array of profile handles.


## -returns



If the function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. If the function is not successful, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Only the Windows default CMM is required to export this function; it is optional for all other CMMs.

If a CMM does not support <b>CMCreateDeviceLinkProfile</b>, Windows uses the default CMM to create a device link profile.

The first and the last profiles in the array must be <a href="d.htm">device profiles</a>. The other profiles can be <a href="c.htm">color space</a> or abstract profiles. Each profile's output color space must be the next profile's input color space.

The calling application must free the buffer allocated by this function and pointed to by the <i>lpProfileData</i> parameter. Use the <b>GlobalFree</b> function to free the buffer.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>
 

 

