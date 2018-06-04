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

# IWICImageEncoder::WriteThumbnail


## -description


Encodes the given image as the thumbnail to the given WIC bitmap encoder.


## -parameters




### -param pImage [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.


### -param pEncoder [in]

Type: <b><a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>*</b>

The encoder on which the thumbnail is set.


### -param pImageParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/0B461697-C7ED-48C9-A880-1B5F4A26FCFC">WICImageParameters</a>*</b>

Additional parameters to control encoding.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must create the image that you pass in on the same device as in <a href="https://msdn.microsoft.com/1F75030F-68B0-4333-B3CF-C4ABD8969448">IWICImagingFactory2::CreateImageEncoder</a>. If you don't specify additional parameters in the variable that <i>pImageParameters</i> points to, the encoder uses a set of useful defaults. For info about these defaults, see <a href="https://msdn.microsoft.com/0B461697-C7ED-48C9-A880-1B5F4A26FCFC">WICImageParameters</a>. 

Before you call <b>WriteThumbnail</b>, you must set up the <a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a> interface for the encoder on which you want to set the thumbnail. 

If <b>WriteThumbnail</b> fails, it might return E_OUTOFMEMORY, D2DERR_WRONG_RESOURCE_DOMAIN, or other error codes from the encoder.




## -see-also




<a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a>



<a href="https://msdn.microsoft.com/1F75030F-68B0-4333-B3CF-C4ABD8969448">IWICImagingFactory2::CreateImageEncoder</a>



<a href="https://msdn.microsoft.com/0B461697-C7ED-48C9-A880-1B5F4A26FCFC">WICImageParameters</a>
 

 

