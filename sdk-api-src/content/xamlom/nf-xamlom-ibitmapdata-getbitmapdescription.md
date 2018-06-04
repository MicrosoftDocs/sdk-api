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

# IBitmapData::GetBitmapDescription


## -description


Gets a <a href="https://msdn.microsoft.com/C5E1BA37-738C-4251-8648-681C58B740E1">BitmapDescription</a> that describes the bitmap data stored in the <a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>.


## -parameters




### -param pBitmapDescription [out]

Information about the bitmap stored in the <a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>
 

 

