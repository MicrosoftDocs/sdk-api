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

# ITransferSource::SetProperties


## -description


Sets properties that should be applied to an item.


## -parameters




### -param pproparray [in]

Type: <b><a href="https://msdn.microsoft.com/c7de40d0-9fe6-4c4b-ba17-c4648501ce0a">IPropertyChangeArray</a>*</b>

An array of properties and their changed values.


## -returns



Type: <b>HRESULT</b>

Any return value other than S_OK indicates a failure.



