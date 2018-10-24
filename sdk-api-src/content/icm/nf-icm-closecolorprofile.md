---
UID: NF:icm.CloseColorProfile
title: CloseColorProfile function
author: windows-sdk-content
description: This CloseColorProfile closes an open profile handle.
old-location: wcs\closecolorprofile.htm
tech.root: WCS
ms.assetid: 49656afa-64fc-4421-8948-34a65c9f829e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CloseColorProfile, CloseColorProfile function [Windows Color System], _color_CloseColorProfile, icm/CloseColorProfile, wcs.closecolorprofile
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
 - Mscms.dll
api_name:
 - CloseColorProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseColorProfile function


## -description


This <b>CloseColorProfile</b> closes an open profile handle.


## -parameters




### -param hProfile

Handle to the profile to be closed. The function determines whether the HPROFILE contains ICC or WCS profile information.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

