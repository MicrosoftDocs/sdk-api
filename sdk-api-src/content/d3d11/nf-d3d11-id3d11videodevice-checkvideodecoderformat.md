---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ID3D11VideoDevice::CheckVideoDecoderFormat


## -description


Given aprofile, checks whether the driver supports a specified output format.


## -parameters




### -param pDecoderProfile [in]

A pointer to a GUID that identifies the profile. To get the list of supported profiles, call <a href="https://msdn.microsoft.com/8D958469-7FC3-4B4F-82BF-271662CF0088">ID3D11VideoDevice::GetVideoDecoderProfile</a>.


### -param Format [in]

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> value that specifies the output format. Typical values include <b>DXGI_FORMAT_NV12</b> and <b>DXGI_FORMAT_420_OPAQUE</b>.


### -param pSupported [out]

Receives the value <b>TRUE</b> if the format is supported, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the driver does not support the profile given in <i>pDecoderProfile</i>, the method returns <b>E_INVALIDARG</b>. If the driver supports the profile, but the DXGI format is not compatible with the profile, the method succeeds but returns the value <b>FALSE</b> in <i>pSupported</i>. 




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

