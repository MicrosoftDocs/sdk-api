---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnWriteCompleted
title: IRDPSRAPITransportStreamEvents::OnWriteCompleted (rdpencomapi.h)
author: windows-sdk-content
description: Notifies the Remote Desktop Protocol (RDP) stack that a write operation has completed.
old-location: rdp\irdpsrapitransportstreamevents_onwritecompleted.htm
tech.root: rdp
ms.assetid: 19d99eba-e7ee-4bdc-8a9f-2cac97d17dea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnWriteCompleted method, IRDPSRAPITransportStreamEvents.OnWriteCompleted, IRDPSRAPITransportStreamEvents::OnWriteCompleted, OnWriteCompleted, OnWriteCompleted method [RDP], OnWriteCompleted method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onwritecompleted, rdpencomapi/IRDPSRAPITransportStreamEvents::OnWriteCompleted
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
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPITransportStreamEvents.OnWriteCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPITransportStreamEvents::OnWriteCompleted


## -description


Notifies the Remote Desktop Protocol (RDP) stack that a write operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.


## -parameters




### -param pBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the stream buffer that was written.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>



<a href="https://msdn.microsoft.com/9e78360d-9ea6-4a74-8a20-5546057c24b0">WriteBuffer</a>
 

 

