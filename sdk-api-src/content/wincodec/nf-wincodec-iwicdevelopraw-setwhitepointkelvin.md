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

# IWICDevelopRaw::SetWhitePointKelvin


## -description


Sets the white point Kelvin value.


## -parameters




### -param WhitePointKelvin [in]

Type: <b>UINT</b>

The white point Kelvin value. Acceptable Kelvin values are 1,500 through 30,000.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Codec implementers should faithfully adjust the color temperature within the range supported natively by the raw image. For values outside the native support range, the codec implementer should provide a best effort representation of the image at that color temperature.

Codec implementers should return <b>WINCODEC_ERR_VALUEOUTOFRANGE</b> if the value is out of defined acceptable range.

Codec implementers must ensure proper interoperability with other white point setting methods such as <a href="https://msdn.microsoft.com/7059959f-dcd6-46a6-a95c-1dd9610f865c">SetWhitePointRGB</a>. For example, if the caller sets the white point via <a href="https://msdn.microsoft.com/eb83233d-7967-4160-bebf-2b06378f77ab">SetNamedWhitePoint</a> then the codec implementer may want to disable reading back the correspoinding Kelvin temperature. In specific cases where the codec implementer wants to deny a given action because of previous calls, <b>WINCODEC_ERR_WRONGSTATE</b> should be returned.



