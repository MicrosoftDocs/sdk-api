---
UID: NF:vfw.AVIFileCreateStreamW
title: AVIFileCreateStreamW function
author: windows-sdk-content
description: The AVIFileCreateStream function creates a new stream in an existing file and creates an interface to the new stream.
old-location: multimedia\avifilecreatestream.htm
tech.root: Multimedia
ms.assetid: bff87fbb-fcd8-4dd4-93d0-9cab39c30409
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AVIFileCreateStream, AVIFileCreateStream function [Windows Multimedia], AVIFileCreateStreamA, AVIFileCreateStreamW, _win32_AVIFileCreateStream, multimedia.avifilecreatestream, vfw/AVIFileCreateStream, vfw/AVIFileCreateStreamA, vfw/AVIFileCreateStreamW
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
req.unicode-ansi: AVIFileCreateStreamW (Unicode) and AVIFileCreateStreamA (ANSI)
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
 - AVIFileCreateStream
 - AVIFileCreateStreamA
 - AVIFileCreateStreamW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIFileCreateStreamW function


## -description



The <b>AVIFileCreateStream</b> function creates a new stream in an existing file and creates an interface to the new stream.




## -parameters




### -param pfile

Handle to an open AVI file.


### -param ppavi

Pointer to the new stream interface.


### -param psi

Pointer to a structure containing information about the new stream, including the stream type and its sample rate.


## -returns



Returns zero if successful or an error otherwise. Unless the file has been opened with write permission, this function returns AVIERR_READONLY.




## -remarks



This function starts a reference count for the new stream.

The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface. The argument <i>ppavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/7a1ba29b-e8ba-435d-a551-c9184631971c">AVIStreamInfo</a>
 

 

