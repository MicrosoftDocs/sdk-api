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

# IWMPPlugin::AdviseWMPServices


## -description



The <b>IWMPPlugin::AdviseWMPServices</b> method is implemented by the plug-in.




## -parameters




### -param pWMPServices [in]

Pointer to an <b>IWMPServices</b> interface.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Windows Media Player calls the <b>AdviseWMPServices</b> method on the plug-in to pass in a pointer that the plug-in can then use to call the <b>IWMPServices</b> interface, which contains methods that provide information about the current state of the stream.




## -see-also




<a href="https://msdn.microsoft.com/e384aa43-72ab-44b7-b6bd-7a29335b5197">IWMPPlugin Interface</a>



<a href="https://msdn.microsoft.com/26d68b4b-4eeb-42e2-a1d1-0d0e73725059">IWMPServices Interface</a>
 

 

