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

# IWICImagingFactory::CreateColorTransformer


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/6c8ae787-3175-4128-ae9f-e11cb0e4c317">IWICColorTransform</a> class.


## -parameters




### -param ppIWICColorTransform [out]

Type: <b><a href="https://msdn.microsoft.com/6c8ae787-3175-4128-ae9f-e11cb0e4c317">IWICColorTransform</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/6c8ae787-3175-4128-ae9f-e11cb0e4c317">IWICColorTransform</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



