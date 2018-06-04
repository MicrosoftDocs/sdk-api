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

# IWMPPlugin::UnAdviseWMPServices


## -description



The <b>IWMPPlugin::UnAdviseWMPServices</b> method is used to release the pointer provided by <b>AdviseWMPServices</b>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player calls this method when the pointer provided by <b>AdviseWMPServices</b> is no longer valid. The plug-in should use this method to cease making stream state requests through the pointer.




## -see-also




<a href="https://msdn.microsoft.com/e384aa43-72ab-44b7-b6bd-7a29335b5197">IWMPPlugin Interface</a>



<a href="https://msdn.microsoft.com/203b9363-1363-48be-8ba6-8b152ae9a92f">IWMPPlugin::AdviseWMPServices</a>
 

 

