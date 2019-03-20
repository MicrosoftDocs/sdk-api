---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnReadCompleted
title: IRDPSRAPITransportStreamEvents::OnReadCompleted (rdpencomapi.h)
author: windows-sdk-content
description: Notifies the Remote Desktop Protocol (RDP) stack that a read operation has completed.
old-location: rdp\irdpsrapitransportstreamevents_onreadcompleted.htm
tech.root: rdp
ms.assetid: 27c3a16a-3d78-46b1-b328-1a1b6f059687
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnReadCompleted method, IRDPSRAPITransportStreamEvents.OnReadCompleted, IRDPSRAPITransportStreamEvents::OnReadCompleted, OnReadCompleted, OnReadCompleted method [RDP], OnReadCompleted method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onreadcompleted, rdpencomapi/IRDPSRAPITransportStreamEvents::OnReadCompleted
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
 - IRDPSRAPITransportStreamEvents.OnReadCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

