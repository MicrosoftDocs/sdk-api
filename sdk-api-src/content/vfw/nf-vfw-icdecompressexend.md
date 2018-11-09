---
UID: NF:vfw.ICDecompressExEnd
title: ICDecompressExEnd macro
author: windows-sdk-content
description: The ICDecompressExEnd macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the ICM_DECOMPRESSEX_END message.
old-location: multimedia\icdecompressexend.htm
tech.root: Multimedia
ms.assetid: db0ab881-2e26-4f60-a22c-cb4bd2016028
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ICDecompressExEnd, ICDecompressExEnd macro [Windows Multimedia], _win32_ICDecompressExEnd, multimedia.icdecompressexend, vfw/ICDecompressExEnd
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
 - ICDecompressExEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressExEnd macro


## -description



The <b>ICDecompressExEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/7ed63a4e-bb17-43a3-b593-25c4a51be942">ICM_DECOMPRESSEX_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver frees any resources allocated for the <a href="https://msdn.microsoft.com/35298274-91b5-4df0-b4b0-4a71d6a49990">ICM_DECOMPRESSEX_BEGIN</a> message.


<a href="https://msdn.microsoft.com/35277938-6fae-4207-8b91-439af2b481e8">ICM_DECOMPRESSEX_BEGIN</a> and <a href="https://msdn.microsoft.com/7ed63a4e-bb17-43a3-b593-25c4a51be942">ICM_DECOMPRESSEX_END</a> do not nest. If your driver receives <a href="https://msdn.microsoft.com/35298274-91b5-4df0-b4b0-4a71d6a49990">ICM_DECOMPRESSEX_BEGIN</a> before decompression is stopped with <b>ICM_DECOMPRESSEX_END</b>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

