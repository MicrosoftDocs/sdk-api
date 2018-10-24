---
UID: NF:icm.GetColorProfileHeader
title: GetColorProfileHeader function
author: windows-sdk-content
description: The GetColorProfileHeader function retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.
old-location: wcs\getcolorprofileheader.htm
tech.root: WCS
ms.assetid: 7006cae0-0166-4fd9-8bf9-f0f0ed249956
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetColorProfileHeader, GetColorProfileHeader function [Windows Color System], _color_GetColorProfileHeader, icm/GetColorProfileHeader, wcs.getcolorprofileheader
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
 - GetColorProfileHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetColorProfileHeader function


## -description


The <b>GetColorProfileHeader</b> function retrieves or derives ICC header structure from either ICC color profile or WCS XML profile. Drivers and applications should assume returning <b>TRUE</b> only indicates that a properly structured header is returned. Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.


## -parameters




### -param hProfile

Specifies a handle to the color profile in question.


### -param pHeader

Points to a variable in which the ICC header structure is to be placed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. This function will fail is an invalid ICC or WCS XML profile is referenced in the hProfile parameter. For extended error information, call <b>GetLastError</b>.




## -remarks



To determine whether the header is derived from an ICC or DMP profile handle, check the header signature (header bytes 36-39). If the signature is "acsp" (big endian) then an ICC profile was used. If the signature is "cdmp" (big-endian) then a DMP was used.

The distinguishing features that identify a header as having been "synthesized" for a WCS DMP are:

pIcmProfileHeader-&gt;phSignature = 'pmdc' (little endian = big endian 'cdmp')

pIcmProfileHeader-&gt;phCMMType = '1scw' (little endian = big endian 'wcs1').




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/bf17bd8a-6ab5-45f8-89c3-797dd090dd6f">PROFILEHEADER</a>
 

 

