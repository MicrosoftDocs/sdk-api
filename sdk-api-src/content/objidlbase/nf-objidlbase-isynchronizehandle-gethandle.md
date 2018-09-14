---
UID: NF:objidlbase.ISynchronizeHandle.GetHandle
title: ISynchronizeHandle::GetHandle
author: windows-sdk-content
description: Retrieves a handle to the synchronization object.
old-location: com\isynchronizehandle_gethandle.htm
tech.root: com
ms.assetid: 951bc2e4-2ef9-48cf-91a1-1a39c2361f42
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetHandle, GetHandle method [COM], GetHandle method [COM],ISynchronizeHandle interface, ISynchronizeHandle interface [COM],GetHandle method, ISynchronizeHandle.GetHandle, ISynchronizeHandle::GetHandle, _com_isynchronizehandle_gethandle, com.isynchronizehandle_gethandle, objidlbase/ISynchronizeHandle::GetHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
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
 - objidlbase.h
api_name:
 - ISynchronizeHandle.GetHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronizeHandle::GetHandle


## -description


Retrieves a handle to the synchronization object.


## -parameters




### -param ph [out]

A pointer to the variable that receives a handle to the synchronization object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e278930c-4f4d-4ac5-ba1e-a4a84bfcd0ca">ISynchronizeEvent::SetEventHandle</a>



<a href="https://msdn.microsoft.com/93b2e682-78da-4a61-a045-8d71b3834e1d">ISynchronizeHandle</a>
 

 

