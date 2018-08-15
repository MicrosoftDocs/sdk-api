---
UID: NF:comsvcs.IComQCEvents.OnQCPlayback
title: IComQCEvents::OnQCPlayback
author: windows-sdk-content
description: Generated when a messages contents are replayed.
old-location: cos\icomqcevents_onqcplayback.htm
old-project: cossdk
ms.assetid: 7cd9daf8-cc4d-4d48-b547-95b370f5a927
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComQCEvents interface [COM+],OnQCPlayback method, IComQCEvents.OnQCPlayback, IComQCEvents::OnQCPlayback, OnQCPlayback, OnQCPlayback method [COM+], OnQCPlayback method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCPlayback, comsvcs/IComQCEvents::OnQCPlayback, cos.icomqcevents_onqcplayback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComQCEvents.OnQCPlayback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComQCEvents::OnQCPlayback


## -description


Generated when a messages contents are replayed.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param objid [in]

The just-in-time activated object.


### -param guidMsgId [in]

The unique identifier for the queue.


### -param guidWorkFlowId [in]

This parameter is reserved.


### -param hr [in]

The status from Message Queuing receive message.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

