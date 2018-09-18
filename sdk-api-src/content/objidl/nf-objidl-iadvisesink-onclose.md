---
UID: NF:objidl.IAdviseSink.OnClose
title: IAdviseSink::OnClose
author: windows-sdk-content
description: Called by the server to notify all registered advisory sinks that the object has changed from the running to the loaded state.
old-location: com\iadvisesink_onclose.htm
tech.root: com
ms.assetid: a695c623-4a4e-4f3d-9f12-ee198c0761a9
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IAdviseSink interface [COM],OnClose method, IAdviseSink.OnClose, IAdviseSink::OnClose, OnClose, OnClose method [COM], OnClose method [COM],IAdviseSink interface, _ole_iadvisesink_onclose, com.iadvisesink_onclose, objidl/IAdviseSink::OnClose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IAdviseSink.OnClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAdviseSink::OnClose


## -description


Called by the server to notify all registered advisory sinks that the object has changed from the running to the loaded state.




## -parameters






## -returns



This method does not return a value.




## -remarks



The <b>OnClose</b> notification indicates that an object is making the transition from the running to the loaded state, so its container can take appropriate measures to ensure an orderly shutdown. For example, an object handler must release its pointer to the object.

If the object that is closing is the last open object supported by its OLE server application, the application can also shut down.

In the case of a link object, the notification that the object is closing should always be interpreted to mean that the connection to the link source has broken.




## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>
 

 

