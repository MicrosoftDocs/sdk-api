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

# IBDA_EasMessage::get_EasMessage


## -description


The <b>get_EasMessage</b> method retrieves an EAS message.


## -parameters




### -param ulEventID [in]

Specifies the event ID of the EAS message.


### -param ppEASObject [in, out]

Pointer to a pointer variable that receives a pointer to the <b>IUnknown</b> interface of the EAS object. The caller can query this object for its <a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method retrieves a counted reference to an <b>IUnknown</b> interface instance. The caller is responsible for releasing the interface when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/dfacaa47-c844-434f-951a-9ee38fa8af4a">IBDA_EasMessage Interface</a>
 

 

