---
UID: NF:icm.GetColorProfileFromHandle
title: GetColorProfileFromHandle function
author: windows-sdk-content
description: Given a handle to an open color profile, the GetColorProfileFromHandle function will copy the contents of the profile into a buffer supplied by the application.
old-location: wcs\getcolorprofilefromhandle.htm
tech.root: WCS
ms.assetid: ff51c6d5-4db2-4b64-a4e3-34a9e502f456
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetColorProfileFromHandle, GetColorProfileFromHandle function [Windows Color System], _color_GetColorProfileFromHandle, icm/GetColorProfileFromHandle, wcs.getcolorprofilefromhandle
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
 - GetColorProfileFromHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetColorProfileFromHandle function


## -description


Given a handle to an open color profile, the <b>GetColorProfileFromHandle</b> function will copy the contents of the profile into a buffer supplied by the application. If the handle is a Windows Color System (WCS) handle, then the DMP is returned and the CAMP and GMMP associated with the HPROFILE are ignored.


## -parameters




### -param hProfile

Handle to an open color profile. The function determines whether the HPROFILE contains ICC or WCS profile information.


### -param pProfile

TBD


### -param pcbProfile

TBD




#### - pBuffer

Pointer to buffer to receive raw ICC or DMP profile data. Can be <b>NULL</b>. If it is, the size required for the buffer will be stored in the memory location pointed to by <i>pcbSize</i>. The buffer can be allocated to the appropriate size, and this function called again with <i>pBuffer</i> containing the address of the buffer.


#### - pcbSize

Pointer to a <b>DWORD</b> that holds the size of buffer pointed at by <i>pBuffer</i>. On return it is filled with size of buffer that was actually used if the function succeeds. If this function is called with <i>pBuffer</i> set to <b>NULL</b>, this parameter will contain the size of the buffer required.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It returns <b>FALSE</b> if the <i>pBuffer</i> parameter is <b>NULL</b> and the size required for the buffer is copied into <i>pcbSize.</i>

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

