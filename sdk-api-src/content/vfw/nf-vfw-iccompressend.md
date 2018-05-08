---
UID: NF:vfw.ICCompressEnd
title: ICCompressEnd macro
author: windows-driver-content
description: The ICCompressEnd macro notifies a video compression driver to end compression and free resources allocated for compression. You can use this macro or explicitly call the ICM_COMPRESS_END message.
old-location: multimedia\iccompressend.htm
old-project: Multimedia
ms.assetid: 04daaf34-63c3-40c1-9ed6-2ae07558d1b8
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ICCompressEnd, ICCompressEnd macro [Windows Multimedia], _win32_ICCompressEnd, multimedia.iccompressend, vfw/ICCompressEnd
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICCompressEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICCompressEnd macro


## -description



The <b>ICCompressEnd</b> macro notifies a video compression driver to end compression and free resources allocated for compression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/5d4b5962-c4f0-44eb-a3a9-36026f167a5a">ICM_COMPRESS_END</a> message.




## -parameters




### -param hic

Handle of the compressor. 


## -remarks



VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. <b>ICCompressBegin</b> and <b>ICCompressEnd</b> do not nest. If your driver receives the <b>ICM_COMPRESS_BEGIN</b> message before compression is stopped with the <b>ICM_COMPRESS_END</b> message, it should restart compression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

