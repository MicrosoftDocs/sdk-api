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

# IWICMetadataHandlerInfo::GetContainerFormats


## -description


Retrieves the container formats supported by the metadata handler.


## -parameters




### -param cContainerFormats [in]

Type: <b>UINT</b>

The size of the <i>pguidContainerFormats</i> array.


### -param pguidContainerFormats [in, out]

Type: <b>GUID*</b>

Pointer to an array that receives the container formats supported by the metadata handler.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual number of GUIDs added to the array.
               

To obtain the number of supported container formats, pass <code>NULL</code> to <i>pguidContainerFormats</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



