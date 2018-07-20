---
UID: NF:vfw.AVIStreamInfoA
title: AVIStreamInfoA function
author: windows-sdk-content
description: The AVIStreamInfo function obtains stream header information.
old-location: multimedia\avistreaminfo.htm
old-project: Multimedia
ms.assetid: 7a1ba29b-e8ba-435d-a551-c9184631971c
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: AVIStreamInfo, AVIStreamInfo function [Windows Multimedia], AVIStreamInfoA, AVIStreamInfoW, _win32_AVIStreamInfo, multimedia.avistreaminfo, vfw/AVIStreamInfo, vfw/AVIStreamInfoA, vfw/AVIStreamInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AVIStreamInfoW (Unicode) and AVIStreamInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamInfo
 - AVIStreamInfoA
 - AVIStreamInfoW
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamInfoA function


## -description



The <b>AVIStreamInfo</b> function obtains stream header information.




## -parameters




### -param pavi

Handle to an open stream.


### -param psi

Pointer to a structure to contain the stream information.


### -param lSize

Size, in bytes, of the structure used forpsi.


## -returns



Returns zero if successful or an error otherwise.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

