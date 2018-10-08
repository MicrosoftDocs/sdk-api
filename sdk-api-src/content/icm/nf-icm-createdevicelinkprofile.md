---
UID: NF:icm.CreateDeviceLinkProfile
title: CreateDeviceLinkProfile function
author: windows-sdk-content
description: The CreateDeviceLinkProfile function creates an International Color Consortium (ICC) device link profile from a set of color profiles, using the specified intents.
old-location: wcs\createdevicelinkprofile.htm
tech.root: WCS
ms.assetid: 6b47e190-ff8a-411e-9c6e-9a421a0f25ef
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: CreateDeviceLinkProfile, CreateDeviceLinkProfile function [Windows Color System], _color_CreateDeviceLinkProfile, icm/CreateDeviceLinkProfile, wcs.createdevicelinkprofile
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mscms.dll
api_name:
 - CreateDeviceLinkProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDeviceLinkProfile function


## -description


The <a href="https://msdn.microsoft.com/54f46d2c-ddcb-4597-9816-172e507a7fa2">CreateDeviceLinkProfile</a> function creates an International Color Consortium (ICC) <i>device link profile</i> from a set of color profiles, using the specified intents.


## -parameters




### -param hProfile

TBD


### -param nProfiles

Specifies the number of profiles in the array pointed to by <i>pahProfiles</i>. 


### -param padwIntent

Pointer to an array of <b>DWORDS</b> containing the intents to be used. See <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>. 


### -param nIntents

The number of intents in the array pointed to by <i>padwIntent</i>. 


### -param dwFlags

Specifies flags to used control creation of the transform. For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>. 


### -param pProfileData

Pointer to a pointer to a buffer. If successful, this function allocates the buffer, places its address in <i>*pProfileData</i>, and fills it with a device link profile. If the function succeeds, the calling application must free the buffer after it is no longer needed. 


### -param indexPreferredCMM

Specifies the one-based index of the color profile that indicates what color management module (CMM) to use. The application developer may allow Windows to choose the CMM by setting this parameter to INDEX_DONT_CARE. See <a href="https://msdn.microsoft.com/df119e1a-b6f5-40a3-8852-8a57b21483d0">Using Color Management Modules (CMM)</a>. 


#### - pahProfiles

Pointer to an array of handles of the color profiles to be used. The function determines whether the HPROFILEs contain ICC profile information and, if so, it processes them appropriately. 


## -returns



If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. For extended error information, call GetLastError.




## -remarks



For HPROFILEs that contain WCS profile information, the HPROFILEs are converted into valid ICC profile handles and then these ICC profile handles are used in creating the device link profile.

The first and the last profiles in the array must be device profiles. The other profiles can be color space or abstract profiles.

Each profile's output color space must be the next profile's input color space.

The calling application must free the buffer allocated by this function and pointed to by the <i>pProfileData</i> parameter. The <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function should be used to free the buffer.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>
 

 

