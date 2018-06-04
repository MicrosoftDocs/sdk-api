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

# IMFMediaEngineExtension::CancelObjectCreation


## -description


Cancels the current request to create an object.


## -parameters




### -param pIUnknownCancelCookie [in]

The pointer that was returned in the the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">IMFMediaEngineExtension::BeginCreateObject</a> method.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method attempts to cancel a previous call to <a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">BeginCreateObject</a>. Because that method is asynchronous, however, it might complete before the operation can be canceled.




## -see-also




<a href="https://msdn.microsoft.com/A032E0D0-2201-4B81-9FE0-8E9CE2707FDB">IMFMediaEngineExtension</a>
 

 

