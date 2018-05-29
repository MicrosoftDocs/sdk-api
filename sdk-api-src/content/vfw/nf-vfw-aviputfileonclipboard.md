---
UID: NF:vfw.AVIPutFileOnClipboard
title: AVIPutFileOnClipboard function
author: windows-sdk-content
description: The AVIPutFileOnClipboard function copies an AVI file to the clipboard.
old-location: multimedia\aviputfileonclipboard.htm
old-project: Multimedia
ms.assetid: 5b2bf73d-9a09-4eec-bbb2-893fe584e3e0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AVIPutFileOnClipboard, AVIPutFileOnClipboard function [Windows Multimedia], _win32_AVIPutFileOnClipboard, multimedia.aviputfileonclipboard, vfw/AVIPutFileOnClipboard
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Avifil32.dll
api_name:
-	AVIPutFileOnClipboard
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIPutFileOnClipboard function


## -description



The <b>AVIPutFileOnClipboard</b> function copies an AVI file to the clipboard.




## -parameters




### -param pf

Handle to an open AVI file.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



This function also copies data with the CF_DIB, CF_PALETTE, and CF_WAVE clipboard flags onto the clipboard using the first frame of the first video stream of the file as a DIB and using the audio stream as CF_WAVE.

The argument pf is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

