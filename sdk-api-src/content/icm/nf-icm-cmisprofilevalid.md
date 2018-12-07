---
UID: NF:icm.CMIsProfileValid
title: CMIsProfileValid function
author: windows-sdk-content
description: The CMIsProfileValid function reports whether the given profile is a valid ICC profile that can be used for color management.
old-location: wcs\cmisprofilevalid.htm
tech.root: WCS
ms.assetid: 3b4ce918-fa51-48a1-9026-c8e76e7015a5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMIsProfileValid, CMIsProfileValid function [Windows Color System], _color_CMIsProfileValid, icm/CMIsProfileValid, wcs.cmisprofilevalid
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
 - CMIsProfileValid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMIsProfileValid
: 
---

# CMIsProfileValid function


## -description


The <b>CMIsProfileValid</b> function reports whether the given profile is a valid ICC profile that can be used for color management.


## -parameters




### -param hProfile

Specifies the profile to check.


### -param lpbValid

Pointer to a variable that is set on exit to <b>TRUE</b> if the profile is a valid ICC profile, or <b>FALSE</b> if not.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. If the function fails, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Only the Windows default CMM is required to export this function; it is optional for all other CMMs.

If a CMM does not support this function, Windows uses the default CMM to validate the profile.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

