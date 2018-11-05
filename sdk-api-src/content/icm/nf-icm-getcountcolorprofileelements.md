---
UID: NF:icm.GetCountColorProfileElements
title: GetCountColorProfileElements function
author: windows-sdk-content
description: The GetCountColorProfileElements function retrieves the number of tagged elements in a given color profile.
old-location: wcs\getcountcolorprofileelements.htm
tech.root: WCS
ms.assetid: f8df63ff-9c8c-4131-b38d-ee39c9160a06
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetCountColorProfileElements, GetCountColorProfileElements function [Windows Color System], _color_GetCountColorProfileElements, icm/GetCountColorProfileElements, wcs.getcountcolorprofileelements
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
 - GetCountColorProfileElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCountColorProfileElements function


## -description


The <b>GetCountColorProfileElements</b> function retrieves the number of tagged elements in a given color profile.


## -parameters




### -param hProfile

Specifies a handle to the profile in question.


### -param pnElementCount

TBD




#### - pnCount

Pointer to a variable in which to place the number of tagged elements in the profile.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

