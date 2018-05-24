---
UID: NF:vfw.AVIStreamGetFrame
title: AVIStreamGetFrame function
author: windows-driver-content
description: The AVIStreamGetFrame function returns the address of a decompressed video frame.
old-location: multimedia\avistreamgetframe.htm
old-project: Multimedia
ms.assetid: 9677efee-4c40-4acd-8911-eedcbee67d6b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AVIStreamGetFrame, AVIStreamGetFrame function [Windows Multimedia], _win32_AVIStreamGetFrame, multimedia.avistreamgetframe, vfw/AVIStreamGetFrame
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Avifil32.dll
-	Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
-	AVIStreamGetFrame
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamGetFrame function


## -description



The <b>AVIStreamGetFrame</b> function returns the address of a decompressed video frame.




## -parameters




### -param pg

TBD


### -param lPos

Position, in samples, within the stream of the desired frame.


#### - pgf

Pointer to the <a href="https://msdn.microsoft.com/d72349bc-5e7c-4c60-b8e0-0524d02c0583">IGetFrame</a> interface.


## -returns



Returns a pointer to the frame data if successful or <b>NULL</b> otherwise. The frame data is returned as a packed DIB.




## -remarks



The returned frame is valid only until the next call to this function or the <a href="https://msdn.microsoft.com/cd1fa615-ab09-4d58-9d6d-a1843c0f1d7a">AVIStreamGetFrameClose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

