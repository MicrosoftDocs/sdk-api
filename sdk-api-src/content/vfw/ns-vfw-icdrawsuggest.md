---
UID: NS:vfw.ICDRAWSUGGEST
title: ICDRAWSUGGEST
author: windows-sdk-content
description: The ICDRAWSUGGEST structure contains compression parameters used with the ICM_DRAW_SUGGESTFORMAT message to suggest an appropriate input format.
old-location: multimedia\icdrawsuggest.htm
old-project: Multimedia
ms.assetid: d8dab197-7364-4f90-b08e-c913df85723e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICDRAWSUGGEST, ICDRAWSUGGEST structure [Windows Multimedia], _win32_ICDRAWSUGGEST_str, multimedia.icdrawsuggest, vfw/ICDRAWSUGGEST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: ICDRAWSUGGEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDRAWSUGGEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDRAWSUGGEST structure


## -description



The <b>ICDRAWSUGGEST</b> structure contains compression parameters used with the <a href="https://msdn.microsoft.com/e3e97790-dbd1-4436-9830-5218ae1f949b">ICM_DRAW_SUGGESTFORMAT</a> message to suggest an appropriate input format.




## -struct-fields




### -field lpbiIn

Pointer to the structure containing the compressed input format.


### -field lpbiSuggest

Pointer to a buffer to return a compatible input format for the renderer.


### -field dxSrc

Width of the source rectangle.


### -field dySrc

Height of the source rectangle.


### -field dxDst

Width of the destination rectangle.


### -field dyDst

Height of the destination rectangle.


### -field hicDecompressor

Handle to a decompressor that supports the format of data described in <b>lpbiIn</b>.


## -see-also




<a href="https://msdn.microsoft.com/e3e97790-dbd1-4436-9830-5218ae1f949b">ICM_DRAW_SUGGESTFORMAT</a>



Video Compression Manager



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

