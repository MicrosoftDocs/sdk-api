---
UID: NF:bdatif.IGuideDataEvent.ServiceDeleted
title: IGuideDataEvent::ServiceDeleted
author: windows-sdk-content
description: The ServiceDeleted method is called when a service has been deleted.
old-location: mstv\iguidedataevent_servicedeleted.htm
tech.root: MSTV
ms.assetid: bba15ebe-d1c5-4c71-b052-6b75a7825613
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ServiceDeleted method, IGuideDataEvent.ServiceDeleted, IGuideDataEvent::ServiceDeleted, IGuideDataEventServiceDeleted, ServiceDeleted, ServiceDeleted method [Microsoft TV Technologies], ServiceDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ServiceDeleted, mstv.iguidedataevent_servicedeleted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataEvent.ServiceDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent::ServiceDeleted


## -description



The <b>ServiceDeleted</b> method is called when a service has been deleted.



Currently the <a href="https://msdn.microsoft.com/en-us/library/Dd693011(v=VS.85).aspx">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.


## -parameters




### -param varServiceDescriptionID [in]

Specifies the unique identifier of the service that was deleted.


## -returns



Return S_OK if successful, or an error code.




## -remarks



The event sink is not required to support this event; it may return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent Interface</a>
 

 

