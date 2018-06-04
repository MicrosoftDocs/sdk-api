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

# ITraceRelogger::Inject


## -description


The <b>Inject</b> method injects a non-system-generated event into the event stream being written to the output trace logfile.


## -parameters




### -param Event [in]

Type: <b>IEvent*</b>

The event to be injected into the stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is the primary way to indicate which events should go into the output trace logfile.

To preserve an existing event provided by <a href="https://msdn.microsoft.com/2099db80-89fd-4ce1-a7ca-e79abbd7b9e5">IEventCallback::OnEvent</a>, this method should be called.




## -see-also




<a href="https://msdn.microsoft.com/2099db80-89fd-4ce1-a7ca-e79abbd7b9e5">IEventCallback::OnEvent</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

