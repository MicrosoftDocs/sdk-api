---
UID: NF:objidl.IAdviseSink.OnSave
title: IAdviseSink::OnSave method
author: windows-driver-content
description: Called by the server to notify all registered advisory sinks that the object has been saved.
old-location: com\iadvisesink_onsave.htm
old-project: com
ms.assetid: 26da5e16-5790-49c0-ba63-5feee49cd4c6
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IAdviseSink, IAdviseSink interface [COM], OnSave method, IAdviseSink::OnSave, OnSave method [COM], OnSave method [COM], IAdviseSink interface, OnSave,IAdviseSink.OnSave, _ole_iadvisesink_onsave, com.iadvisesink_onsave, objidl/IAdviseSink::OnSave
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IAdviseSink.OnSave
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAdviseSink::OnSave method


## -description


Called by the server to notify all registered advisory sinks that the object has been saved.


## -parameters






## -returns



This method does not return a value.




## -remarks



Object handlers and link objects normally implement <b>IAdviseSink::OnSave</b> to receive notifications of when an object is saved to disk, either to its original storage (through a <b>Save</b> operation) or to new storage (through a <b>Save As</b> operation). Object Handlers and link objects register to be notified when an object is saved for the purpose of updating their caches, but then only if the advise flag passed during registration specifies ADVFCACHE_ONSAVE. Object handlers and link objects forward these notifications to their containers.




## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>
 

 

