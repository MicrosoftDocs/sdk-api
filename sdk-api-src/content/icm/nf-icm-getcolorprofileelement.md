---
UID: NF:icm.GetColorProfileElement
title: GetColorProfileElement function
author: windows-sdk-content
description: The GetColorProfileElement function copies data from a specified tagged profile element of a specified color profile into a buffer.
old-location: wcs\getcolorprofileelement.htm
tech.root: WCS
ms.assetid: 37bcfafc-7316-4c72-80df-c3424d639181
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetColorProfileElement, GetColorProfileElement function [Windows Color System], _color_GetColorProfileElement, icm/GetColorProfileElement, wcs.getcolorprofileelement
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
 - GetColorProfileElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetColorProfileElement function


## -description


The <b>GetColorProfileElement</b> function copies data from a specified tagged profile element of a specified color profile into a buffer.


## -parameters




### -param hProfile

Specifies a handle to the International Color Consortium (ICC) color profile in question.


### -param tag

Identifies the tagged element from which to copy.


### -param dwOffset

Specifies the offset from the first byte of the tagged element data at which to begin copying.


### -param pcbElement

TBD


### -param pElement

TBD


### -param pbReference

Points to a Boolean value that is set to <b>TRUE</b> if more than one tag in the color profile refers to the same data as the specified tag refers to, or <b>FALSE</b> if not.


#### - pBuffer

Pointer to a buffer into which the tagged element data is to be copied. The buffer must contain at least as many bytes as are specified by the variable pointed to by <i>pcbSize</i>. If the <i>pBuffer</i> pointer is set to <b>NULL</b>, the size of the entire tagged element data in bytes is returned in the memory location pointed to by <i>pcbSize,</i> and <i>dwOffset</i> is ignored. In this case, the function will return <b>FALSE</b>.


#### - pcbSize

Pointer to a variable specifying the number of bytes to copy. On return, the variable contains the number of bytes actually copied.


## -returns



If this function succeeds, the return value is nonzero.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid International Color Consortium (ICC) profile.

If the <i>pBuffer</i> pointer is set to <b>NULL</b>, the size of the entire tagged element data in bytes is returned in the variable pointed to by <i>pcbSize,</i> and <i>dwOffset</i> is ignored.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with, and hard coded to, ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

