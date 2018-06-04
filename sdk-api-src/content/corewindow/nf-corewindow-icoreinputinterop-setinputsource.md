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

# ICoreInputInterop::SetInputSource


## -description


Sets the input source for an app's <a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a> or <a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>.


## -parameters




### -param value [in]

Pointer to the base COM interface of the input source.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>



<a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a>



<a href="https://msdn.microsoft.com/F7BA7EFB-D9DC-4FF2-97A4-C4818BCBD599">ICoreInputInterop</a>
 

 

