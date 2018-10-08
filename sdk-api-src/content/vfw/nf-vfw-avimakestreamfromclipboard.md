---
UID: NF:vfw.AVIMakeStreamFromClipboard
title: AVIMakeStreamFromClipboard function
author: windows-sdk-content
description: The AVIMakeStreamFromClipboard function creates an editable stream from stream data on the clipboard.
old-location: multimedia\avimakestreamfromclipboard.htm
tech.root: Multimedia
ms.assetid: e41f4ef2-bb57-4a92-b382-7faa106d2aa0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: AVIMakeStreamFromClipboard, AVIMakeStreamFromClipboard function [Windows Multimedia], _win32_AVIMakeStreamFromClipboard, multimedia.avimakestreamfromclipboard, vfw/AVIMakeStreamFromClipboard
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
 - AVIMakeStreamFromClipboard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIMakeStreamFromClipboard function


## -description



The <b>AVIMakeStreamFromClipboard</b> function creates an editable stream from stream data on the clipboard.




## -parameters




### -param cfFormat

Clipboard flag.


### -param hGlobal

Handle to stream data on the clipboard.


### -param ppstream

Handle to the created stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



When an application finishes using the editable stream, it must release the stream to free the resources associated with it.

The argument ppstream is the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

