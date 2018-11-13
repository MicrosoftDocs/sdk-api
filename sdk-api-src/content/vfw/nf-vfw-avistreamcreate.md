---
UID: NF:vfw.AVIStreamCreate
title: AVIStreamCreate function
author: windows-sdk-content
description: The AVIStreamCreate function creates a stream not associated with any file.
old-location: multimedia\avistreamcreate.htm
tech.root: Multimedia
ms.assetid: 8c784875-dc8f-4fd4-b267-0194cdbfa3c7
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AVIStreamCreate, AVIStreamCreate function [Windows Multimedia], _win32_AVIStreamCreate, multimedia.avistreamcreate, vfw/AVIStreamCreate
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
 - AVIStreamCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamCreate function


## -description



The <b>AVIStreamCreate</b> function creates a stream not associated with any file.




## -parameters




### -param ppavi

Pointer to a buffer that receives the new stream interface.


### -param lParam1

Stream-handler specific information.


### -param lParam2

Stream-handler specific information.


### -param pclsidHandler

Pointer to the class identifier used for the stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



You should not need to call this function. Some functions, such as <a href="https://msdn.microsoft.com/9c7b0ebe-c113-49c9-a74f-61f47e7c18af">CreateEditableStream</a> and <a href="https://msdn.microsoft.com/63279d7e-0e64-4708-a29c-60d5fdf75cb2">AVIMakeCompressedStream</a>, use it internally.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

