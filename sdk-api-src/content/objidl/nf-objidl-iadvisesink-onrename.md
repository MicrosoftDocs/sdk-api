---
UID: NF:objidl.IAdviseSink.OnRename
title: IAdviseSink::OnRename
author: windows-sdk-content
description: Called by the server to notify all registered advisory sinks that the object has been renamed.
old-location: com\iadvisesink_onrename.htm
old-project: com
ms.assetid: ec9926fb-d69e-430c-b67d-24c52d806bb5
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IAdviseSink interface [COM],OnRename method, IAdviseSink.OnRename, IAdviseSink::OnRename, OnRename, OnRename method [COM], OnRename method [COM],IAdviseSink interface, _ole_iadvisesink_onrename, com.iadvisesink_onrename, objidl/IAdviseSink::OnRename
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IAdviseSink.OnRename
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAdviseSink::OnRename


## -description


Called by the server to notify all registered advisory sinks that the object has been renamed.




## -parameters




### -param pmk [in]

 A pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the new full moniker of the object.


## -returns



This method does not return a value.




## -remarks



OLE link objects normally implement <b>IAdviseSink::OnRename</b> to receive notification of a change in the name of a link source or its container. The object serving as the link source calls <b>OnRename</b> and passes its new full moniker to the object handler, which forwards the notification to the link object. In response, the link object must update its moniker. The link object, in turn, forwards the notification to its own container.




## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>
 

 

