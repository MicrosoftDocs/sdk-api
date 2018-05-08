---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnReadCompleted
title: IRDPSRAPITransportStreamEvents::OnReadCompleted
author: windows-driver-content
description: Notifies the Remote Desktop Protocol (RDP) stack that a read operation has completed.
old-location: rdp\irdpsrapitransportstreamevents_onreadcompleted.htm
old-project: Rdp
ms.assetid: 27c3a16a-3d78-46b1-b328-1a1b6f059687
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnReadCompleted method, IRDPSRAPITransportStreamEvents.OnReadCompleted, IRDPSRAPITransportStreamEvents::OnReadCompleted, OnReadCompleted, OnReadCompleted method [RDP], OnReadCompleted method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onreadcompleted, rdpencomapi/IRDPSRAPITransportStreamEvents::OnReadCompleted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPSRAPITransportStreamEvents.OnReadCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRDPSRAPITransportStreamEvents::OnReadCompleted


## -description


Notifies the Remote Desktop Protocol (RDP) stack that a read operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.


## -parameters




### -param pBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the stream buffer that was read.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>



<a href="https://msdn.microsoft.com/0a6d9a76-48b8-4755-985e-efbef01a6382">ReadBuffer</a>
 

 

