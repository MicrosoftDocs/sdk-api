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

# IWICMetadataReaderInfo::GetPatterns


## -description


Gets the metadata patterns associated with the metadata reader.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The cointainer format GUID.


### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of the <i>pPattern</i> buffer.


### -param pPattern [in, out]

Type: <b><a href="https://msdn.microsoft.com/cea9e07d-5e55-4320-9744-b5864b58cfd6">WICMetadataPattern</a>*</b>

Pointer that receives the metadata patterns.


### -param pcCount [in, out]

Type: <b>UINT*</b>

Pointer that receives the number of metadata patterns.


### -param pcbActual [in, out]

Type: <b>UINT*</b>

Pointer that receives the size, in bytes, needed to obtain the metadata patterns.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



