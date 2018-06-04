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

# IWICBitmapCodecInfo::GetPixelFormats


## -description


Retrieves the pixel formats the codec supports.


## -parameters




### -param cFormats [in]

Type: <b>UINT</b>

The size of the <i>pguidPixelFormats</i> array. Use <code>0</code> on first call to determine the needed array size.


### -param pguidPixelFormats [in, out]

Type: <b>GUID*</b>

Receives the supported pixel formats. Use <code>NULL</code> on first call to determine needed array size.


### -param pcActual [out]

Type: <b>UINT*</b>

The array size needed to retrieve all supported pixel formats.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            The usage pattern for this method is a two call process.
            The first call retrieves the array size needed to retrieve all the supported pixel formats by calling it with <i>cFormats</i> set to <code>0</code> and <i>pguidPixelFormats</i> set to <code>NULL</code>.
            This call sets <i>pcActual</i> to the array size needed.
            Once the needed array size is determined, a second <b>GetPixelFormats</b> call with <i>pguidPixelFormats</i> set to an array of the appropriate size will retrieve the pixel formats.
         



