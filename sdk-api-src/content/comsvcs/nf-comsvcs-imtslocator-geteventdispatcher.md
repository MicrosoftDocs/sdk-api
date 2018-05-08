---
UID: NF:comsvcs.IMTSLocator.GetEventDispatcher
title: IMTSLocator::GetEventDispatcher
author: windows-driver-content
description: Retrieves a pointer to the event dispatcher for the current process.
old-location: cos\imtslocator_geteventdispatcher.htm
old-project: cossdk
ms.assetid: 10e110bf-1a7c-48a2-ab9f-836ea21d442b
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetEventDispatcher, GetEventDispatcher method [COM+], GetEventDispatcher method [COM+],IMTSLocator interface, IMTSLocator interface [COM+],GetEventDispatcher method, IMTSLocator.GetEventDispatcher, IMTSLocator::GetEventDispatcher, _dtc_IMtsLocator_GetEventDispatcher, comsvcs/IMTSLocator::GetEventDispatcher, cos.imtslocator_geteventdispatcher
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMTSLocator.GetEventDispatcher
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMTSLocator::GetEventDispatcher


## -description


Retrieves a pointer to the event dispatcher for the current process.


## -parameters




### -param pUnk [out]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the event dispatcher for the current process.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/afa559bc-5ac2-4487-bb13-25f30c5f4033">IMTSLocator</a>
 

 

