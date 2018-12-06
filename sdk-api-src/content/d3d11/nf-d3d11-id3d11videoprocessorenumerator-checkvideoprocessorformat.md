---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat
title: ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat
author: windows-sdk-content
description: Queries whether the video processor supports a specified video format.
old-location: mf\id3d11videoprocessorenumerator_checkvideoprocessorformat.htm
tech.root: medfound
ms.assetid: 75DE439B-6849-4413-BF7D-0EBADA96F097
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CheckVideoProcessorFormat, CheckVideoProcessorFormat method [Media Foundation], CheckVideoProcessorFormat method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],CheckVideoProcessorFormat method, ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat, ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat, d3d11/ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat, mf.id3d11videoprocessorenumerator_checkvideoprocessorformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator.CheckVideoProcessorFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoProcessorEnumerator::CheckVideoProcessorFormat


## -description


Queries whether the video processor supports a specified video format.


## -parameters




### -param Format [in]

The video format to query, specified as a <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> value.


### -param pFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/A23C33B8-20D0-4F78-B21F-36FCD1506DC6">D3D11_VIDEO_PROCESSOR_FORMAT_SUPPORT</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

