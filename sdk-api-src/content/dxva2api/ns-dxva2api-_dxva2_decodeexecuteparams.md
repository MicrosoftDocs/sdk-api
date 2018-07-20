---
UID: NS:dxva2api._DXVA2_DecodeExecuteParams
title: "_DXVA2_DecodeExecuteParams"
author: windows-sdk-content
description: Contains parameters for the IDirectXVideoDecoder::Execute method.
old-location: mf\dxva2_decodeexecuteparams.htm
old-project: medfound
ms.assetid: e0e95e9b-6d53-4b90-a933-243023dc31ef
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXVA2_DecodeExecuteParams, DXVA2_DecodeExecuteParams structure [Media Foundation], _DXVA2_DecodeExecuteParams, dxva2api/DXVA2_DecodeExecuteParams, e0e95e9b-6d53-4b90-a933-243023dc31ef, mf.dxva2_decodeexecuteparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVA2_DecodeExecuteParams
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_DecodeExecuteParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA2_DecodeExecuteParams structure


## -description



Contains parameters for the <a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">IDirectXVideoDecoder::Execute</a> method.




## -struct-fields




### -field NumCompBuffers

Number of compressed buffers.


### -field pCompressedBuffers

Pointer to an array of <a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a> structures that describe the compressed buffers. The number of elements in the array is given by the <b>NumCompBuffers</b> member.


### -field pExtensionData

Pointer to a <a href="https://msdn.microsoft.com/2a1b7139-fcbb-40b0-9ed3-f9b1fe482358">DXVA2_DecodeExtensionData</a> structure that contains private data. Set this member to <b>NULL</b> unless you need to send private data to or from the driver.


## -see-also




<a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

