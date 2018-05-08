---
UID: NF:d3d10.ID3D10Device.CheckFormatSupport
title: ID3D10Device::CheckFormatSupport
author: windows-driver-content
description: Get the support of a given format on the installed video device.
old-location: direct3d10\id3d10device_checkformatsupport.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_checkformatsupport.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: CheckFormatSupport, CheckFormatSupport method [Direct3D 10], CheckFormatSupport method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CheckFormatSupport method, ID3D10Device.CheckFormatSupport, ID3D10Device::CheckFormatSupport, d3d10/ID3D10Device::CheckFormatSupport, direct3d10.id3d10device_checkformatsupport, eaf02733-648b-44c6-4ca7-57aa2cecf913
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.CheckFormatSupport
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CheckFormatSupport


## -description


Get the support of a given format on the installed video device.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> enumeration that describes a format for which to check for support.


### -param pFormatSupport [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A bitfield of <a href="https://msdn.microsoft.com/d5f98664-dd8b-4ed5-9f56-dc6d7890aaea">D3D10_FORMAT_SUPPORT</a> enumeration values describing how the specified format is supported on the installed device. 
        The values are ORed together.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Format</i> parameter is <b>NULL</b>, or returns E_FAIL if the described 
      format does not exist.




## -remarks



Most format support is based on the Direct3D feature level. Only a few specific use cases require checking for support. 
      See <a href="https://msdn.microsoft.com/529ced9a-d4fa-4b41-932b-343638cd5c7c">Hardware Support for Direct3D 10 Formats</a> 
      and <a href="https://msdn.microsoft.com/011ad888-1c1d-4cbd-ab70-12fb8adc000f">Hardware Support for Direct3D 10.1 Formats</a> for additional information.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

