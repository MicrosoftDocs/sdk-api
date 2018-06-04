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

# CoRegisterMessageFilter function


## -description


Registers with OLE the instance of an <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface, which is to be used for handling concurrency issues on the current thread. Only one message filter can be registered for each thread. Threads in multithreaded apartments cannot have message filters.


## -parameters




### -param lpMessageFilter [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a> interface on the message filter. This message filter should be registered on the current thread, replacing the previous message filter (if any). This parameter can be <b>NULL</b>, indicating that no message filter should be registered on the current thread.

Note that this function calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the interface pointer to the message filter.


### -param lplpMessageFilter [out, optional]

Address of the <a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>* pointer variable that receives the interface pointer to the previously registered message filter. If there was no previously registered message filter for the current thread, the value of *<i>lplpMessageFilter</i> is <b>NULL</b>.


## -returns



If the instance was registered or revoked successfully, the return value is S_OK; otherwise, it is S_FALSE.




## -remarks



To revoke the registered message filter, pass the previous message filter (possibly <b>NULL</b>) as the <i>lpMessageFilter</i> parameter to <b>CoRegisterMessageFilter</b>.





## -see-also




<a href="https://msdn.microsoft.com/e12d48c0-5033-47a8-bdcd-e94c49857248">IMessageFilter</a>
 

 

