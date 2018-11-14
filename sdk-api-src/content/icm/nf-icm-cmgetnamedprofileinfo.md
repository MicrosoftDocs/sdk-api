---
UID: NF:icm.CMGetNamedProfileInfo
title: CMGetNamedProfileInfo function
author: windows-sdk-content
description: The CMGetNamedProfileInfo function retrieves information about the specified named color profile.
old-location: wcs\cmgetnamedprofileinfo.htm
tech.root: WCS
ms.assetid: 9791d32f-b343-4da7-add3-ed7bcecfd010
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CMGetNamedProfileInfo, CMGetNamedProfileInfo function [Windows Color System], _color_CMGetNamedProfileInfo, icm/CMGetNamedProfileInfo, wcs.cmgetnamedprofileinfo
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
 - CMGetNamedProfileInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMGetNamedProfileInfo
: 
---

# CMGetNamedProfileInfo function


## -description


The <b>CMGetNamedProfileInfo</b> function retrieves information about the specified named color profile.


## -parameters




### -param hProfile

The handle to the profile from which the information will be retrieved.


### -param pNamedProfileInfo

A pointer to a <b>NAMED_PROFILE_INFO</b> structure.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is required in the default CMM. It is optional for all other CMMs.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/decb0b76-872c-4237-a2b0-6da83d49c8cf">NAMED_PROFILE_INFO</a>
 

 

