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

# RtwqAddPeriodicCallback function


## -description


Sets a callback function to be called at a fixed interval.


## -parameters




### -param Callback [in]

Pointer to the callback function. 


### -param context

Pointer to a caller-provided object that implements <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, or <b>NULL</b>. This parameter is passed to the callback function.


### -param key [out, optional]

Receives a key that can be used to cancel the callback. To cancel the callback, call <a href="https://msdn.microsoft.com/308910e3-dae8-4f23-9782-adf2996a58aa">RtwqRemovePeriodicCallback</a> and pass this key as the <i>dwKey</i> parameter.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



