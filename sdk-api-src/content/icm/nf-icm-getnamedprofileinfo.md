---
UID: NF:icm.GetNamedProfileInfo
title: GetNamedProfileInfo function
author: windows-sdk-content
description: The GetNamedProfileInfo function retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.
old-location: wcs\getnamedprofileinfo.htm
tech.root: WCS
ms.assetid: b3260a41-80c2-4233-9e42-d2e03930bb04
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetNamedProfileInfo, GetNamedProfileInfo function [Windows Color System], _color_GetNamedProfileInfo, icm/GetNamedProfileInfo, wcs.getnamedprofileinfo
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
 - GetNamedProfileInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNamedProfileInfo function


## -description


The <b>GetNamedProfileInfo</b> function retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.


## -parameters




### -param hProfile

The handle to the ICC profile from which the information will be retrieved.


### -param pNamedProfileInfo

A pointer to a <b>NAMED_PROFILE_INFO</b> structure.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/decb0b76-872c-4237-a2b0-6da83d49c8cf">NAMED_PROFILE_INFO</a>
 

 

