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

# IWMPServices::GetStreamState


## -description



The <b>IWMPServices::GetStreamState</b> method retrieves information about the current play state of the stream.




## -parameters




### -param pState [in]

A pointer to a <b>WMPServices_StreamState</b> enumeration value.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



The stream is stopped, paused, or playing.




## -see-also




<a href="https://msdn.microsoft.com/26d68b4b-4eeb-42e2-a1d1-0d0e73725059">IWMPServices Interface</a>



<a href="https://msdn.microsoft.com/82c4699a-197c-4429-afa8-b1fc47a1f47a">WMPServices_StreamState</a>
 

 

