---
UID: NF:vfw.AVIGetFromClipboard
title: AVIGetFromClipboard function
author: windows-sdk-content
description: The AVIGetFromClipboard function copies an AVI file from the clipboard.
old-location: multimedia\avigetfromclipboard.htm
old-project: Multimedia
ms.assetid: 17115441-8809-4fc2-9749-0e9d4c4f9cac
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AVIGetFromClipboard, AVIGetFromClipboard function [Windows Multimedia], _win32_AVIGetFromClipboard, multimedia.avigetfromclipboard, vfw/AVIGetFromClipboard
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
req.unicode-ansi: 
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
api_name:
 - AVIGetFromClipboard
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIGetFromClipboard function


## -description



The <b>AVIGetFromClipboard</b> function copies an AVI file from the clipboard.




## -parameters




### -param lppf

Pointer to the location used to return the handle created for the AVI file.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



If the clipboard does not contain an AVI file, <b>AVIGetFromClipboard</b> also can copy data with the CF_DIB or CF_WAVE clipboard flags to an AVI file. In this case, the function creates an AVI file with one DIB stream and one waveform-audio stream, and fills each stream with the data from the clipboard.

The argument <i>lppf</i> is the address of a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

