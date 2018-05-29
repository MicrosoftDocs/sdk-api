---
UID: NF:vfw.AVIStreamBeginStreaming
title: AVIStreamBeginStreaming function
author: windows-sdk-content
description: The AVIStreamBeginStreaming function specifies the parameters used in streaming and lets a stream handler prepare for streaming.
old-location: multimedia\avistreambeginstreaming.htm
old-project: Multimedia
ms.assetid: 79bf7c19-56b6-48fa-a673-32ce1bcdddad
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AVIStreamBeginStreaming, AVIStreamBeginStreaming function [Windows Multimedia], _win32_AVIStreamBeginStreaming, multimedia.avistreambeginstreaming, vfw/AVIStreamBeginStreaming
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
-	AVIStreamBeginStreaming
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamBeginStreaming function


## -description



The <b>AVIStreamBeginStreaming</b> function specifies the parameters used in streaming and lets a stream handler prepare for streaming.




## -parameters




### -param pavi

Pointer to a stream.


### -param lStart

Starting frame for streaming.


### -param lEnd

Ending frame for streaming.


### -param lRate

Speed at which the file is read relative to its natural speed. Specify 1000 for the normal speed. Values less than 1000 indicate a slower-than-normal speed; values greater than 1000 indicate a faster-than-normal speed.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

