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

# IMFQualityAdviseLimits::GetMinimumQualityLevel


## -description


Gets the minimum quality level that is supported by the component.


## -parameters




### -param peQualityLevel [out]

Receives the minimum quality level, specified as a member of the <a href="https://msdn.microsoft.com/6fe5abbb-c079-4d74-9c75-6fb502054546">MF_QUALITY_LEVEL</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the current quality level, call the <a href="https://msdn.microsoft.com/9a2b501e-543d-4ba0-86a1-a55e7d136685">IMFQualityAdvise::GetQualityLevel</a> method. To set the quality level, call the <a href="https://msdn.microsoft.com/f788fd7d-65fc-4917-8d5d-cfaf35a013e7">IMFQualityAdvise::SetQualityLevel</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8ef7088c-2f49-4be9-b719-481616e1737d">IMFQualityAdviseLimits</a>
 

 

