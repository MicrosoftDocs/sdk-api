---
UID: NF:comsvcs.IDispenserManager.GetContext
title: IDispenserManager::GetContext
author: windows-sdk-content
description: Determines the current context.
old-location: cos\idispensermanager_getcontext.htm
tech.root: cossdk
ms.assetid: cc3095a3-df4c-4112-a3cb-308e8962b51f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetContext, GetContext method [COM+], GetContext method [COM+],IDispenserManager interface, IDispenserManager interface [COM+],GetContext method, IDispenserManager.GetContext, IDispenserManager::GetContext, _dtc_IDispenserManager_GetContext, comsvcs/IDispenserManager::GetContext, cos.idispensermanager_getcontext
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IDispenserManager.GetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDispenserManager::GetContext


## -description


Determines the current context.


## -parameters




### -param __MIDL__IDispenserManager0002 [out]

An internal unique identifier of the current object, or 0 if no current object. This may not be interpreted as an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer to the current object.


### -param __MIDL__IDispenserManager0003 [out]

The transaction that the current object is running in, or 0 if none. This value may be cast to <b>ITransaction *</b>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>
 

 

