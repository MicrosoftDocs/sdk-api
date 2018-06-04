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

# IWICComponentFactory::CreateEncoderPropertyBag


## -description


Creates an encoder property bag.


## -parameters




### -param ppropOptions [in]

Type: <b><a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a>*</b>

Pointer to an array of <a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a> options used to create the encoder property bag.


### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a> structures in the <i>ppropOptions</i> array.


### -param ppIPropertyBag [out]

Type: <b><a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>**</b>

A pointer that receives a pointer to an encoder <a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



