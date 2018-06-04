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

# AmsiInitialize function


## -description


Initialize the AMSI API.


## -parameters




### -param appName [in]

The name, version, or GUID string of the app calling the AMSI API.


### -param amsiContext [out]

A handle of type HAMSICONTEXT that must be passed to all subsequent calls to the AMSI API.


#### - coInit [in]

Ignored. This parameter may be removed from a future build of Windows 10.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the app is finished with the AMSI API it must call <a href="https://msdn.microsoft.com/DAC1AAE6-3160-4A82-8E81-9CB245AFD653">AmsiUninitialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/DAC1AAE6-3160-4A82-8E81-9CB245AFD653">AmsiUninitialize</a>
 

 

