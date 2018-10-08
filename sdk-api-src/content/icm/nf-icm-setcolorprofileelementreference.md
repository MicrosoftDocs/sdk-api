---
UID: NF:icm.SetColorProfileElementReference
title: SetColorProfileElementReference function
author: windows-sdk-content
description: SetColorProfileElementReference creates in a specified ICC color profile a new tag which references the same data as an existing tag.
old-location: wcs\setcolorprofileelementreference.htm
tech.root: WCS
ms.assetid: 385a291c-6c15-4b8b-8b48-62d8a6513834
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: SetColorProfileElementReference, SetColorProfileElementReference function [Windows Color System], _color_SetColorProfileElementReference, icm/SetColorProfileElementReference, wcs.setcolorprofileelementreference
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
 - SetColorProfileElementReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetColorProfileElementReference function


## -description


<b>SetColorProfileElementReference</b> creates in a specified ICC color profile a new tag which references the same data as an existing tag.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param newTag

Identifies the new tag to create.


### -param refTag

Identifies the existing tag whose data is to be referenced by the new tag.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

If <i>newTag</i> already exists or <i>refTag</i> does not exist, <b>SetColorProfileElementReference</b> fails.

If the color profile was not opened with read/write permission, <b>SetColorProfileElementReference</b> fails.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

