---
UID: NF:vfw.AVIStreamStart
title: AVIStreamStart function
author: windows-sdk-content
description: The AVIStreamStart function returns the starting sample number for the stream.
old-location: multimedia\avistreamstart.htm
tech.root: Multimedia
ms.assetid: d4c66732-f777-44c7-9d61-88b721e150c1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AVIStreamStart, AVIStreamStart function [Windows Multimedia], _win32_AVIStreamStart, multimedia.avistreamstart, vfw/AVIStreamStart
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
 - AVIStreamStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamStart function


## -description



The <b>AVIStreamStart</b> function returns the starting sample number for the stream.




## -parameters




### -param pavi

Handle to an open stream.


## -returns



Returns the number if successful or -1 otherwise.




## -remarks



The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

