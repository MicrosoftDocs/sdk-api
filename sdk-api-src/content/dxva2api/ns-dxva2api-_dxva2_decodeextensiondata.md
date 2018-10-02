---
UID: NS:dxva2api._DXVA2_DecodeExtensionData
title: "_DXVA2_DecodeExtensionData"
author: windows-sdk-content
description: Contains private data for the IDirectXVideoDecoder::Execute method.
old-location: mf\dxva2_decodeextensiondata.htm
tech.root: MedFound
ms.assetid: 2a1b7139-fcbb-40b0-9ed3-f9b1fe482358
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 2a1b7139-fcbb-40b0-9ed3-f9b1fe482358, DXVA2_DecodeExtensionData, DXVA2_DecodeExtensionData structure [Media Foundation], _DXVA2_DecodeExtensionData, dxva2api/DXVA2_DecodeExtensionData, mf.dxva2_decodeextensiondata
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_DecodeExtensionData
product: Windows
targetos: Windows
req.typenames: DXVA2_DecodeExtensionData
req.redist: 
---

# _DXVA2_DecodeExtensionData structure


## -description



Contains private data for the <a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">IDirectXVideoDecoder::Execute</a> method.




## -struct-fields




### -field Function

Function number. This can be zero if this argument is the default or is ignored.


### -field pPrivateInputData

Pointer to private input data passed to the driver.


### -field PrivateInputDataSize

Length of the private input data, in bytes.


### -field pPrivateOutputData

Pointer to private output data passed from the driver to the decoder.


### -field PrivateOutputDataSize

Size of the private output data, in bytes.


## -remarks



This structure corresponds to parameters of the <b>IAMVideoAccelerator::Execute</b> method in DirectX Video Acceleration (DXVA) version 1.




## -see-also




<a href="https://msdn.microsoft.com/e0e95e9b-6d53-4b90-a933-243023dc31ef">DXVA2_DecodeExecuteParams</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

