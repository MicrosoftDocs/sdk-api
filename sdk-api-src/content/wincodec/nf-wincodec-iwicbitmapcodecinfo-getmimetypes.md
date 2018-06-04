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

# IWICBitmapCodecInfo::GetMimeTypes


## -description


Retrieves a comma delimited sequence of mime types associated with the codec.


## -parameters




### -param cchMimeTypes [in]

Type: <b>UINT</b>

The size of the mime types buffer.  Use <code>0</code> on first call to determine needed buffer size.


### -param wzMimeTypes [out]

Type: <b>WCHAR*</b>

Receives the mime types associated with the codec. Use <code>NULL</code> on first call to determine needed buffer size.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve all mime types associated with the codec.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            The usage pattern for this method is a two call process.
            The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchMimeTypes</i> set to <code>0</code> and <i>wzMimeTypes</i> set to <code>NULL</code>.
            This call sets <i>pcchActual</i> to the buffer size needed.
            Once the needed buffer size is determined, a second <b>GetMimeTypes</b> call with <i>cchMimeTypes</i> set to the buffer size and <i>wzMimeTypes</i> set to a buffer of the appropriate size will retrieve the pixel formats.
         



