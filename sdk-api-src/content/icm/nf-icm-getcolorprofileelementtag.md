---
UID: NF:icm.GetColorProfileElementTag
title: GetColorProfileElementTag function
author: windows-sdk-content
description: The GetColorProfileElementTag function retrieves the tag name specified by dwIndex in the tag table of a given International Color Consortium (ICC) color profile, where dwIndex is a one-based index into that table.
old-location: wcs\getcolorprofileelementtag.htm
tech.root: WCS
ms.assetid: 6f3172ac-19e0-43c7-a0a7-587ae31ec2fa
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: GetColorProfileElementTag, GetColorProfileElementTag function [Windows Color System], _color_GetColorProfileElementTag, icm/GetColorProfileElementTag, wcs.getcolorprofileelementtag
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
 - GetColorProfileElementTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetColorProfileElementTag function


## -description


The <b>GetColorProfileElementTag</b> function retrieves the tag name specified by <i>dwIndex</i> in the tag table of a given International Color Consortium (ICC) color profile, where <i>dwIndex</i> is a one-based index into that table.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param dwIndex

Specifies the one-based index of the tag to retrieve.


### -param pTag

Pointer to a variable in which the tag name is to be placed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

<b>GetColorProfileElementTag</b> can be used to enumerate all tags in a profile after getting the number of tags in the profile using <a href="https://msdn.microsoft.com/f8df63ff-9c8c-4131-b38d-ee39c9160a06">GetCountColorProfileElements</a>.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with, and hard coded to, ICC tag types and there exist many robust XML parsing libraries.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

