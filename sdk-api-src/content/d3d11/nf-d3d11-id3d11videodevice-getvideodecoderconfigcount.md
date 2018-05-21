---
UID: NF:d3d11.ID3D11VideoDevice.GetVideoDecoderConfigCount
title: ID3D11VideoDevice::GetVideoDecoderConfigCount
author: windows-driver-content
description: Gets the number of decoder configurations that the driver supports for a specified video description.
old-location: mf\id3d11videodevice_getvideodecoderconfigcount.htm
old-project: medfound
ms.assetid: C6650546-2F6D-4B91-888D-3A5A1AE86DCB
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetVideoDecoderConfigCount, GetVideoDecoderConfigCount method [Media Foundation], GetVideoDecoderConfigCount method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],GetVideoDecoderConfigCount method, ID3D11VideoDevice.GetVideoDecoderConfigCount, ID3D11VideoDevice::GetVideoDecoderConfigCount, d3d11/ID3D11VideoDevice::GetVideoDecoderConfigCount, mf.id3d11videodevice_getvideodecoderconfigcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoDevice.GetVideoDecoderConfigCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoDevice::GetVideoDecoderConfigCount


## -description


Gets the number of decoder configurations that the driver supports for a specified video description.


## -parameters




### -param pDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/668D994C-B875-4666-B940-1052A6DE6AA1">D3D11_VIDEO_DECODER_DESC</a> structure that describes the video stream.


### -param pCount [out]

Receives the number of decoder configurations.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To enumerate the decoder configurations, call <a href="https://msdn.microsoft.com/EC3B23BE-0A28-41E6-A515-7801C9E0A4D9">ID3D11VideoDevice::GetVideoDecoderConfig</a>.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

