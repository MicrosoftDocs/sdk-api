---
UID: NF:vfw.ICDecompressEnd
title: ICDecompressEnd macro
author: windows-sdk-content
description: The ICDecompressEnd macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the ICM_DECOMPRESS_END message.
old-location: multimedia\icdecompressend.htm
tech.root: Multimedia
ms.assetid: 9d66174a-b6bd-4bcd-a88a-bb1876bbc510
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ICDecompressEnd, ICDecompressEnd macro [Windows Multimedia], _win32_ICDecompressEnd, multimedia.icdecompressend, vfw/ICDecompressEnd
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDecompressEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressEnd macro


## -description



The <b>ICDecompressEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver should free any resources allocated for the <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> message.

The <a href="https://msdn.microsoft.com/3e9fb4b7-bdc6-402c-a5c6-3f837149c291">ICDecompressBegin</a> and <b>ICDecompressEnd</b> macros do not nest. If your driver receives <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

