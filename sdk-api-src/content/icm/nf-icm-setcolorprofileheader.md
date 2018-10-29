---
UID: NF:icm.SetColorProfileHeader
title: SetColorProfileHeader function
author: windows-sdk-content
description: The SetColorProfileHeader function sets the header data in a specified ICC color profile.
old-location: wcs\setcolorprofileheader.htm
tech.root: WCS
ms.assetid: a174712b-9977-4d3c-8baa-1b6e502db166
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetColorProfileHeader, SetColorProfileHeader function [Windows Color System], _color_SetColorProfileHeader, icm/SetColorProfileHeader, wcs.setcolorprofileheader
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
 - SetColorProfileHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetColorProfileHeader function


## -description


The <b>SetColorProfileHeader</b> function sets the header data in a specified ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param pHeader

Pointer to the profile header data to write to the specified profile.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

If the color profile was not opened with read/write permission, <b>SetColorProfileHeader</b> fails.

<b>SetColorProfileHeader</b> overwrites the current header in the ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/bf17bd8a-6ab5-45f8-89c3-797dd090dd6f">PROFILEHEADER</a>
 

 

