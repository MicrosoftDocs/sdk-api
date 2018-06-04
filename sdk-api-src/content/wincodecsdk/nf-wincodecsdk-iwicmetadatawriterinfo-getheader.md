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

# IWICMetadataWriterInfo::GetHeader


## -description


Gets the metadata header for the metadata writer.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The format container GUID to obtain the header for.


### -param cbSize [in]

Type: <b>UINT</b>

The size of the <i>pHeader</i> buffer.


### -param pHeader [in, out]

Type: <b><a href="https://msdn.microsoft.com/f643b163-55b2-4691-a4eb-fc162949e936">WICMetadataHeader</a>*</b>

Pointer that receives the <a href="https://msdn.microsoft.com/f643b163-55b2-4691-a4eb-fc162949e936">WICMetadataHeader</a>.


### -param pcbActual [in, out]

Type: <b>UINT*</b>

The actual size of the header.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



