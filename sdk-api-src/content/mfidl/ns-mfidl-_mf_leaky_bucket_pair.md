---
UID: NS:mfidl._MF_LEAKY_BUCKET_PAIR
title: "_MF_LEAKY_BUCKET_PAIR"
author: windows-sdk-content
description: Specifies the buffering requirements of a file.
old-location: mf\mf_leaky_bucket_pair.htm
old-project: medfound
ms.assetid: aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MF_LEAKY_BUCKET_PAIR, MF_LEAKY_BUCKET_PAIR structure [Media Foundation], _MF_LEAKY_BUCKET_PAIR, aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e, mf.mf_leaky_bucket_pair, mfidl/MF_LEAKY_BUCKET_PAIR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_LEAKY_BUCKET_PAIR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_LEAKY_BUCKET_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF_LEAKY_BUCKET_PAIR structure


## -description



Specifies the buffering requirements of a file.




## -struct-fields




### -field dwBitrate

Bit rate, in bits per second.


### -field msBufferWindow

Size of the buffer window, in milliseconds.


## -remarks



This structure describes the buffering requirements for content encoded at the bit rate specified in the <b>dwBitrate</b>. The <b>msBufferWindow</b> member indicates how much data should be buffered before starting playback. The size of the buffer in bytes is <b>msBufferWinow</b>×<b>dwBitrate</b> / 8000.




## -see-also




<a href="https://msdn.microsoft.com/6667d32c-36a8-414e-a546-02d00a447b70">MFBYTESTREAM_BUFFERING_PARAMS</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

