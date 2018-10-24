---
UID: NF:icm.SetColorProfileElement
title: SetColorProfileElement function
author: windows-sdk-content
description: The SetColorProfileElement function sets the element data for a tagged profile element in an ICC color profile.
old-location: wcs\setcolorprofileelement.htm
tech.root: WCS
ms.assetid: 9991cdf7-4ab4-49da-b1ea-70dbeff77f4c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: SetColorProfileElement, SetColorProfileElement function [Windows Color System], _color_SetColorProfileElement, icm/SetColorProfileElement, wcs.setcolorprofileelement
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
 - SetColorProfileElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetColorProfileElement function


## -description


The <b>SetColorProfileElement</b> function sets the element data for a tagged profile element in an ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC profile in question.


### -param tag

Identifies the tagged element.


### -param dwOffset

Specifies the offset from the first byte of the tagged element data at which to start writing.


### -param pcbElement

TBD


### -param pElement

TBD




#### - pBuffer

Pointer to a buffer containing the data to write to the tagged element in the color profile.


#### - pcbSize

Pointer to a variable containing the number of bytes of data to write. On return, it contains the number of bytes actually written.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

If the color profile is not opened for read/write permission, this function fails.

If <i>dwOffset</i> exceeds the size set for the specified tagged element, this function fails.

If <i>dwOffset</i> + <i>*pcbSize</i> is greater than the size of the specified element, this function only writes as many bytes as will fit within the current size of the element.

Any existing data in the specified portion of the tagged element is overwritten when this function succeeds.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

