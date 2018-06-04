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

# IAdviseSinkEx::OnViewStatusChange


## -description


Notifies the sink that a view status of an object has changed.


## -parameters




### -param dwViewStatus [in]

The new view status. Possible values are from the <a href="https://msdn.microsoft.com/7b3118af-db29-4eb1-9b1b-38a8ebe42f19">VIEWSTATUS</a> enumeration.


## -returns



This method returns S_OK on success.




## -remarks



It is important that objects call the <a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink:OnViewChange</a> method whenever the object's view changes even when the object is in place active. Containers rely on this notification to keep an object's view up-to-date.




## -see-also




<a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink:OnViewChange</a>



<a href="https://msdn.microsoft.com/d1a52353-dd86-4083-9dbc-3a6f363a1a57">IAdviseSinkEx</a>
 

 

