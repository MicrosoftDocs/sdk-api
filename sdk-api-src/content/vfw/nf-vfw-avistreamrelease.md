---
UID: NF:vfw.AVIStreamRelease
title: AVIStreamRelease function
author: windows-sdk-content
description: The AVIStreamRelease function decrements the reference count of an AVI stream interface handle, and closes the stream if the count reaches zero.
old-location: multimedia\avistreamrelease.htm
tech.root: Multimedia
ms.assetid: bd71ddf6-9d02-463d-9d1c-50605441ad59
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AVIStreamRelease, AVIStreamRelease function [Windows Multimedia], _win32_AVIStreamRelease, multimedia.avistreamrelease, vfw/AVIStreamRelease
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vfw.h
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamRelease
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamRelease function


## -description



The <b>AVIStreamRelease</b> function decrements the reference count of an AVI stream interface handle, and closes the stream if the count reaches zero.



This function supersedes the obsolete <b>AVIStreamClose</b> function.


## -parameters




### -param pavi

Handle to an open stream.


## -returns



Returns the current reference count of the stream. This value should be used only for debugging purposes.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

