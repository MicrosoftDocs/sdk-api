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

# IWICBitmapFrameEncode::Initialize


## -description


Initializes the frame encoder using the given properties.


## -parameters




### -param pIEncoderOptions [in]

Type: <b><a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>*</b>

The set of properties to use for <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> initialization.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you don't want any encoding options, pass <b>NULL</b> for <i>pIEncoderOptions</i>. Otherwise, pass the <a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a> that was provided by <a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a> with updated values.


For a complete list of encoding options supported by the Windows-provided codecs, see <a href="https://msdn.microsoft.com/8D3E4B3A-FA39-475C-B177-61FC81E5FFCC">Native WIC Codecs</a>. 



