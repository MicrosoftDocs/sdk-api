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

# IMFMediaEngineClassFactoryEx::CreateMediaSourceExtension


## -description


Creates an instance of <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a>.


## -parameters




### -param dwFlags [in]

This parameter is reserved and must be set to 0.


### -param pAttr [in]

This method supports the following  Media Foundation attributes:

<ul>
<li>
<a href="https://msdn.microsoft.com/A5783F9B-6261-4384-9484-275F550709E2">MF_MSE_CALLBACK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9A68B650-97C0-4323-ACBF-5C8E496E8566">MF_MSE_BUFFERLIST_CALLBACK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/703A7BF0-A89F-40E9-9440-B8C8E03FDE1A">MF_MSE_ACTIVELIST_CALLBACK</a>
</li>
</ul>

### -param ppMSE [out]

The <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a> which was created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d672ee59-f702-49c7-8ccf-5ba0260c9b23">IMFMediaEngineClassFactoryEx</a>
 

 

