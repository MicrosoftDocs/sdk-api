---
UID: NF:vfw.ICDecompressBegin
title: ICDecompressBegin macro
author: windows-sdk-content
description: The ICDecompressBegin macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the ICM_DECOMPRESS_BEGIN message.
old-location: multimedia\icdecompressbegin.htm
old-project: Multimedia
ms.assetid: 3e9fb4b7-bdc6-402c-a5c6-3f837149c291
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICDecompressBegin, ICDecompressBegin macro [Windows Multimedia], _win32_ICDecompressBegin, multimedia.icdecompressbegin, vfw/ICDecompressBegin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDecompressBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDecompressBegin macro


## -description



The <b>ICDecompressBegin</b> macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the output format. 


## -remarks



When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process <a href="https://msdn.microsoft.com/666f2ebf-80a5-4846-861d-c79c3001c5a0">ICM_DECOMPRESS</a> messages efficiently.

The <b>ICDecompressBegin</b> and <a href="https://msdn.microsoft.com/9d66174a-b6bd-4bcd-a88a-bb1876bbc510">ICDecompressEnd</a> macros do not nest. If your driver receives <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

