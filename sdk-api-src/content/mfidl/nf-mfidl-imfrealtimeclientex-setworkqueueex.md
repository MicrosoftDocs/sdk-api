---
UID: NF:mfidl.IMFRealTimeClientEx.SetWorkQueueEx
title: IMFRealTimeClientEx::SetWorkQueueEx
author: windows-sdk-content
description: Specifies the work queue that this object should use for asynchronous work items.
old-location: mf\imfrealtimeclientex_setworkqueueex.htm
old-project: medfound
ms.assetid: 4F91FD8A-A8B6-4066-A0EB-F764A3BFD8A2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFRealTimeClientEx interface [Media Foundation],SetWorkQueueEx method, IMFRealTimeClientEx.SetWorkQueueEx, IMFRealTimeClientEx::SetWorkQueueEx, SetWorkQueueEx, SetWorkQueueEx method [Media Foundation], SetWorkQueueEx method [Media Foundation],IMFRealTimeClientEx interface, mf.imfrealtimeclientex_setworkqueueex, mfidl/IMFRealTimeClientEx::SetWorkQueueEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFRealTimeClientEx.SetWorkQueueEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRealTimeClientEx::SetWorkQueueEx


## -description


Specifies the work queue that this object should use for asynchronous work items. 


## -parameters




### -param dwMultithreadedWorkQueueId

The work queue identifier.


### -param lWorkItemBasePriority

The base priority for work items.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The object should use the values of <i>dwMultithreadedWorkQueueId</i> and <i>lWorkItemBasePriority</i> when it queues new work items. Use the <a href="https://msdn.microsoft.com/C49818B3-83FF-40CE-B68A-F60F3277F7B8">MFPutWorkItem2</a> or <a href="https://msdn.microsoft.com/A29DC852-AF0F-4269-97FB-DA1F725E7C09">MFPutWorkItemEx2</a> function to queue the work item.




## -see-also




<a href="https://msdn.microsoft.com/EC5CDD23-B862-4DAE-AC01-4926C4FAD89A">IMFRealTimeClientEx</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

