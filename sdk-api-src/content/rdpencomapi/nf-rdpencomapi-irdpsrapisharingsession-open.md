---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.Open
title: IRDPSRAPISharingSession::Open method
author: windows-driver-content
description: Puts the session in an active state.
old-location: rdp\irdpsrapisharingsession_open.htm
old-project: Rdp
ms.assetid: 2c97a37d-5862-4ad3-9029-481ea0a789e0
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPSRAPISharingSession, IRDPSRAPISharingSession interface [RDP], Open method, IRDPSRAPISharingSession2 interface [RDP], Open method, IRDPSRAPISharingSession2::Open, IRDPSRAPISharingSession::Open, Open method [RDP], Open method [RDP], IRDPSRAPISharingSession interface, Open method [RDP], IRDPSRAPISharingSession2 interface, Open,IRDPSRAPISharingSession.Open, rdp.irdpsrapisharingsession_open, rdpencomapi/IRDPSRAPISharingSession2::Open, rdpencomapi/IRDPSRAPISharingSession::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
-	IRDPSRAPISharingSession2.Open
-	IRDPSRAPISharingSession.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IRDPSRAPISharingSession::Open method


## -description


Puts the session in an active state. After this method is called, the listener is started   and incoming connections will be accepted.


## -parameters






## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following are possible values.




## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>



<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 

