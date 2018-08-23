---
UID: NF:vfw.AVIStreamGetFrameClose
title: AVIStreamGetFrameClose function
author: windows-sdk-content
description: The AVIStreamGetFrameClose function releases resources used to decompress video frames.
old-location: multimedia\avistreamgetframeclose.htm
old-project: Multimedia
ms.assetid: cd1fa615-ab09-4d58-9d6d-a1843c0f1d7a
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: AVIStreamGetFrameClose, AVIStreamGetFrameClose function [Windows Multimedia], _win32_AVIStreamGetFrameClose, multimedia.avistreamgetframeclose, vfw/AVIStreamGetFrameClose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vfw.h
req.include-header: 
req.redist: 
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
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamGetFrameClose
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamGetFrameClose function


## -description



The <b>AVIStreamGetFrameClose</b> function releases resources used to decompress video frames.




## -parameters




### -param pg

Handle returned from the <a href="https://msdn.microsoft.com/467560b2-f79f-49ab-b019-d6315f0c2030">AVIStreamGetFrameOpen</a> function. After calling this function, the handle is invalid.


## -returns



Returns zero if successful or an error otherwise.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

