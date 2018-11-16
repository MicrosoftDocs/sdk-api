---
UID: NF:comsvcs.ISendMethodEvents.SendMethodCall
title: ISendMethodEvents::SendMethodCall
author: windows-sdk-content
description: Generated when a method is called through a component interface.
old-location: cos\isendmethodevents_sendmethodcall.htm
tech.root: cossdk
ms.assetid: 730466c8-440c-42ee-899f-0d93007fbf8d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISendMethodEvents interface [COM+],SendMethodCall method, ISendMethodEvents.SendMethodCall, ISendMethodEvents::SendMethodCall, SendMethodCall, SendMethodCall method [COM+], SendMethodCall method [COM+],ISendMethodEvents interface, _cos_ISendMethodEvents_SendMethodCall, comsvcs/ISendMethodEvents::SendMethodCall, cos.isendmethodevents_sendmethodcall
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
 - ISendMethodEvents.SendMethodCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ISendMethodEvents.SendMethodCall
: 
---

# ISendMethodEvents::SendMethodCall


## -description


Generated when a method is called through a component interface.


## -parameters




### -param pIdentity [in]

A pointer to the interface used to call the method.


### -param riid [in]

The ID of the interface used to call the method.


### -param dwMeth [in]

The method called.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/d1437581-8a2b-4e88-aa12-a16eb9f40125">ISendMethodEvents</a>
 

 

