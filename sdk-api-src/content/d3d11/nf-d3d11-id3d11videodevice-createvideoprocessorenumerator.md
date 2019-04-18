---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessorEnumerator
title: ID3D11VideoDevice::CreateVideoProcessorEnumerator (d3d11.h)
author: windows-sdk-content
description: Enumerates the video processor capabilities of the driver.
old-location: mf\id3d11videodevice_createvideoprocessorenumerator.htm
tech.root: medfound
ms.assetid: 992C699D-A499-494E-AEDF-A6688CB14D70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessorEnumerator, CreateVideoProcessorEnumerator method [Media Foundation], CreateVideoProcessorEnumerator method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessorEnumerator method, ID3D11VideoDevice.CreateVideoProcessorEnumerator, ID3D11VideoDevice::CreateVideoProcessorEnumerator, d3d11/ID3D11VideoDevice::CreateVideoProcessorEnumerator, mf.id3d11videodevice_createvideoprocessorenumerator
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
 - ID3D11VideoDevice.CreateVideoProcessorEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoDevice::CreateVideoProcessorEnumerator


## -description


Enumerates the video processor capabilities of the driver.


## -parameters




### -param pDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/A1649897-B368-4D03-9A08-630C8C59E44A">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a> structure that describes the video content.


### -param ppEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the video processor device, pass the <a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a> pointer to the <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a> method.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

