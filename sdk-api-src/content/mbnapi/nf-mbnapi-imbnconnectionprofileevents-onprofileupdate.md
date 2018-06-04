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

# IMbnConnectionProfileEvents::OnProfileUpdate


## -description


A notification method that indicates that profile update operation has completed.


## -parameters




### -param newProfile [in]

An <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface that represents the profile that has changed.  


## -returns



This method must return <b>S_OK</b>.




## -remarks



<b>OnProfileUpdate</b> is called to notify a registered application of the completion of an operation initiated by a call to the <a href="https://msdn.microsoft.com/3243ffec-1897-4f26-853d-81a7198a892d">UpdateProfile</a> method of the <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface, or the <a href="https://msdn.microsoft.com/b9c191cc-aa6f-4548-ad4a-f2b9808c5f23">CreateConnectionProfile</a> of the <a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/235fa0ef-4fc2-4a36-8ad7-2dceb597498f">IMbnConnectionProfileEvents</a>
 

 

