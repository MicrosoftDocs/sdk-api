---
UID: NF:icm.CMCreateProfileW
title: CMCreateProfileW function
author: windows-sdk-content
description: Creates a display color profile from a LOGCOLORSPACE structure.
old-location: wcs\cmcreateprofilew.htm
tech.root: WCS
ms.assetid: 42bd4282-6d15-4cb1-8879-f6c714742c07
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMCreateProfileW, CMCreateProfileW function [Windows Color System], _color_CMCreateProfileW, icm/CMCreateProfileW, wcs.cmcreateprofilew
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
req.lib: Gdi32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMCreateProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMCreateProfileW
: 
---

# CMCreateProfileW function


## -description


<p class="CCE_Message">[<b>CMCreateProfileW</b> is no longer available for use as of Windows Vista.]

Creates a display color profile from a <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a> structure.


## -parameters




### -param lpColorSpace

Points to a logical color space, of which the <b>lcsFilename</b> member will be <b>NULL</b>.


### -param lpProfileData

Points to a pointer to a buffer. If successful the function allocates and fills this buffer. The calling application must free this buffer when it is no longer needed. Use the <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function to free this buffer.


## -returns



Beginning with Windows Vista, the default CMM (Icm32.dll) will return <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will report ERROR_NOT_SUPPORTED.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. If the function is not successful, the CMM should call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the last error to a valid error value defined in Winerror.h.






## -remarks



Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>CMM Implementors are required to implement this method.

Only the Windows default CMM is required to export this function; it is optional for all other CMMs. If a CMM does not support <b>CMCreateProfileW</b>, Windows uses the default CMM to create the profile.

The ANSI version of this function is <a href="https://msdn.microsoft.com/0677e2d0-b8e8-4136-b895-9f120fa51d2c">CMCreateProfile</a>.

The CMM should set all header fields to sensible defaults. This profile should be usable as the input profile in a transform.






## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/0677e2d0-b8e8-4136-b895-9f120fa51d2c">CMCreateProfile</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>
 

 

