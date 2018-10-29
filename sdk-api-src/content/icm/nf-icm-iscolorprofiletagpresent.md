---
UID: NF:icm.IsColorProfileTagPresent
title: IsColorProfileTagPresent function
author: windows-sdk-content
description: The IsColorProfileTagPresent function reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.
old-location: wcs\iscolorprofiletagpresent.htm
tech.root: WCS
ms.assetid: 6cd5fed1-37ee-47b0-991b-f843b3028b17
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IsColorProfileTagPresent, IsColorProfileTagPresent function [Windows Color System], _color_IsColorProfileTagPresent, icm/IsColorProfileTagPresent, wcs.iscolorprofiletagpresent
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
 - mscms.dll
api_name:
 - IsColorProfileTagPresent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsColorProfileTagPresent function


## -description


The <b>IsColorProfileTagPresent</b> function reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC profile in question.


### -param tag

Specifies the ICC tag to check.


### -param pbPresent

Pointer to a variable that is set to <b>TRUE</b> on return if the specified ICC tag is present, or <b>FALSE</b> if not.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

