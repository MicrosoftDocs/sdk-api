---
UID: NF:icm.SetColorProfileElementSize
title: SetColorProfileElementSize function
author: windows-sdk-content
description: SetColorProfileElementSize sets the size of a tagged element in an ICC color profile.
old-location: wcs\setcolorprofileelementsize.htm
tech.root: WCS
ms.assetid: 59552ca3-5b53-465c-9634-a1cc68bb7c3e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetColorProfileElementSize, SetColorProfileElementSize function [Windows Color System], _color_SetColorProfileElementSize, icm/SetColorProfileElementSize, wcs.setcolorprofileelementsize
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
 - SetColorProfileElementSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetColorProfileElementSize function


## -description


<b>SetColorProfileElementSize</b> sets the size of a tagged element in an ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param tagType

TBD


### -param pcbElement

TBD




#### - cbSize

Specifies the size to set the tagged element to. If <i>cbSize</i> is zero, this function deletes the specified tagged element. If the tag is a reference, only the tag table entry is deleted, not the data.


#### - tag

Identifies the tagged element.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

To create a new tagged element in a color profile, use <b>SetColorProfileElementSize</b> to set the size, then use <a href="https://msdn.microsoft.com/9991cdf7-4ab4-49da-b1ea-70dbeff77f4c">SetColorProfileElement</a> to set the element value.

If the specified tag already exists in the profile, <b>SetColorProfileElementSize</b> changes the size of the element by truncating it or adding zeroes at the end as the case may be.

If the specified tag already exists and is a reference to another tag, <b>SetColorProfileElementSize</b> creates a new data area for the tag that is not shared.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/9991cdf7-4ab4-49da-b1ea-70dbeff77f4c">SetColorProfileElement</a>
 

 

