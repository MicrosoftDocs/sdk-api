---
UID: NF:vfw.ICCompressQuery
title: ICCompressQuery macro
author: windows-sdk-content
description: The ICCompressQuery macro queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.
old-location: multimedia\iccompressquery.htm
old-project: Multimedia
ms.assetid: 5e34a830-5e0c-41e5-9e4a-2d827c73ceeb
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ICCompressQuery, ICCompressQuery macro [Windows Multimedia], _win32_ICCompressQuery, multimedia.iccompressquery, vfw/ICCompressQuery
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
 - ICCompressQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICCompressQuery macro


## -description



The <b>ICCompressQuery</b> macro queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/6d0e735e-8252-4507-b8be-1ba87774f637">ICM_COMPRESS_QUERY</a> message.




## -parameters




### -param hic

Handle to a compressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the output format. You can specify zero for this parameter to indicate any output format is acceptable. 


## -remarks



When a driver receives this message, it should examine the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure associated with <i>lpbiInput</i> to determine if it can compress the input format.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

