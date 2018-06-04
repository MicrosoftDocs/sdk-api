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

# IDsAdminNotifyHandler::Initialize


## -description


The <b>IDsAdminNotifyHandler::Initialize</b> method is called to initialize the  notification  handler.


## -parameters




### -param pExtraInfo [in]

Reserved. This parameter will be <b>NULL</b>.


### -param puEventFlags [out]

Pointer to a <b>ULONG</b> value that receives a set of flags that indicate which events the notification handler should receive. This can be a combination of one or more of the following values. If this parameter receives zero, the notification handler will not receive any events.



#### DSA_NOTIFY_DEL

Notify the handler when an object is deleted.



#### DSA_NOTIFY_REN

Notify the handler when an object is  renamed.



#### DSA_NOTIFY_MOV

Notify the handler when an object is moved.



#### DSA_NOTIFY_PROP

Notify the handler when a property is changed.



#### DSA_NOTIFY_ALL

Notify the handler in response to all events.


## -returns



If the method succeeds, <b>S_OK</b> is returned. If the method fails,  a standard <b>HRESULT</b> value is returned.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/d55e1473-8e51-441e-bd22-63208b294e14">IDsAdminNotifyHandler</a>
 

 

