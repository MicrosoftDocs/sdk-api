---
UID: NF:vfw.AVIStreamAddRef
title: AVIStreamAddRef function
author: windows-sdk-content
description: The AVIStreamAddRef function increments the reference count of an AVI stream.
old-location: multimedia\avistreamaddref.htm
tech.root: Multimedia
ms.assetid: 4d5e6b0f-6753-4ac0-b074-51016634cc10
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AVIStreamAddRef, AVIStreamAddRef function [Windows Multimedia], _win32_AVIStreamAddRef, multimedia.avistreamaddref, vfw/AVIStreamAddRef
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
api_name:
 - AVIStreamAddRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamAddRef function


## -description



The <b>AVIStreamAddRef</b> function increments the reference count of an AVI stream.




## -parameters




### -param pavi

Handle to an open AVI stream.


## -returns



Returns the current reference count of the stream. This value should be used only for debugging purposes.




## -remarks



The argument <i>pavi</i> contains a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

