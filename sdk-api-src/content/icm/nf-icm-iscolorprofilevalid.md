---
UID: NF:icm.IsColorProfileValid
title: IsColorProfileValid function
author: windows-sdk-content
description: The IsColorProfileValid function allows an application to determine whether the specified profile is a valid International Color Consortium (ICC) profile or a valid Windows Color System (WCS) profile handle that can be used for color management.
old-location: wcs\iscolorprofilevalid.htm
tech.root: WCS
ms.assetid: 6b8075ae-301c-4b22-8bed-b4bb154ccc9e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IsColorProfileValid, IsColorProfileValid function [Windows Color System], _color_IsColorProfileValid, icm/IsColorProfileValid, wcs.iscolorprofilevalid
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
 - IsColorProfileValid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsColorProfileValid function


## -description


The <b>IsColorProfileValid</b> function allows an application to determine whether the specified profile is a valid International Color Consortium (ICC) profile or a valid Windows Color System (WCS) profile handle that can be used for color management. WCS profile validation does not invoke the underlying device models, but instead simply validates against the XML schema and the schema element range limits.


## -parameters




### -param hProfile

Specifies a handle to the profile to be validated. The function determines whether the HPROFILE contains ICC or WCS profile information.


### -param pbValid

Pointer to a variable that is set to <b>TRUE</b> on return if the operation succeeds and the profile is a valid ICC or WCS profile. If the operation fails or the profile is not valid the variable is <b>FALSE</b>.


## -returns



If this function succeeds and the profile is valid, the return value is <b>TRUE</b>.

If this function fails (or succeeds and the profile is not valid), the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

