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

# IWICBitmapDecoderInfo::GetPatterns


## -description


Retrieves the file pattern signatures supported by the decoder.


## -parameters




### -param cbSizePatterns [in]

Type: <b>UINT</b>

The array size of the <i>pPatterns</i> array.


### -param pPatterns [out]

Type: <b><a href="https://msdn.microsoft.com/6f0cd639-c0db-46e4-b3a3-bc21222d97ee">WICBitmapPattern</a>*</b>

Receives a list of <a href="https://msdn.microsoft.com/6f0cd639-c0db-46e4-b3a3-bc21222d97ee">WICBitmapPattern</a> objects supported by the decoder.


### -param pcPatterns [out]

Type: <b>UINT*</b>

Receives the number of patterns the decoder supports.


### -param pcbPatternsActual [out]

Type: <b>UINT*</b>

Receives the actual buffer size needed to retrieve all pattern signatures supported by the decoder. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




               To retrieve all pattern signatures, this method should first be called with <i>pPatterns</i> set to <code>NULL</code> to retrieve the actual buffer size needed through <i>pcbPatternsActual</i>.
               Once the needed buffer size is known, allocate a buffer of the needed size and call <b>GetPatterns</b> again with the allocated buffer.
            



