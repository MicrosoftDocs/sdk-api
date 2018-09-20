---
UID: NF:shobjidl_core.IObjectWithCancelEvent.GetCancelEvent
title: IObjectWithCancelEvent::GetCancelEvent
author: windows-sdk-content
description: Retrieves an event that will be sent when an operation is canceled.
old-location: shell\IObjectWithCancelEvent_GetCancelEvent.htm
tech.root: shell
ms.assetid: 6aef54b0-a7aa-4ff9-b50f-f84131614853
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetCancelEvent, GetCancelEvent method [Windows Shell], GetCancelEvent method [Windows Shell],IObjectWithCancelEvent interface, IObjectWithCancelEvent interface [Windows Shell],GetCancelEvent method, IObjectWithCancelEvent.GetCancelEvent, IObjectWithCancelEvent::GetCancelEvent, _shell_IObjectWithCancelEvent_GetCancelEvent, shell.IObjectWithCancelEvent_GetCancelEvent, shobjidl_core/IObjectWithCancelEvent::GetCancelEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IObjectWithCancelEvent.GetCancelEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithCancelEvent::GetCancelEvent


## -description


Retrieves an event that will be sent when an operation is canceled.


## -parameters




### -param phEvent [out]

Type: <b>HANDLE*</b>

Pointer to a handle that, when this method successfully returns, is the handle to the cancel event. The caller is responsible for closing this handle when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this function to retrieve an event that will be signaled when the called object cancels the operation it is performing. The caller is responsible for closing the returned handle.




## -see-also




<a href="https://msdn.microsoft.com/3bac219d-d9fd-4259-8f34-032554291327">IObjectWithCancelEvent</a>
 

 

