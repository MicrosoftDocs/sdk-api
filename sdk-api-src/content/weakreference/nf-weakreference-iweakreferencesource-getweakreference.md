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

# IWeakReferenceSource::GetWeakReference


## -description


Retrieves a weak reference from an <a href="https://msdn.microsoft.com/f4b85374-192b-4024-80c2-a46bfebb16c1">IWeakReferenceSource</a>.


## -parameters




### -param weakReference [out, retval]

Type: <b><a href="https://msdn.microsoft.com/fae8bf21-2a38-4e98-9a11-89c548da9e95">IWeakReference</a>**</b>

The weak reference.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f4b85374-192b-4024-80c2-a46bfebb16c1">IWeakReferenceSource</a>
 

 

