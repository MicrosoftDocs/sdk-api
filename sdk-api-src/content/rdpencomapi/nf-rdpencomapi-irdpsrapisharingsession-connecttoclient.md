---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.ConnectToClient
title: IRDPSRAPISharingSession::ConnectToClient
author: windows-sdk-content
description: Used for reverse connect mode, where the sharer connects to the viewer.
old-location: rdp\irdpsrapisharingsession_connecttoclient.htm
old-project: rdp
ms.assetid: 18651433-90cb-4ebd-afaf-480800dfe033
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ConnectToClient, ConnectToClient method [RDP], ConnectToClient method [RDP],IRDPSRAPISharingSession interface, ConnectToClient method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],ConnectToClient method, IRDPSRAPISharingSession.ConnectToClient, IRDPSRAPISharingSession2 interface [RDP],ConnectToClient method, IRDPSRAPISharingSession2::ConnectToClient, IRDPSRAPISharingSession::ConnectToClient, rdp.irdpsrapisharingsession_connecttoclient, rdpencomapi/IRDPSRAPISharingSession2::ConnectToClient, rdpencomapi/IRDPSRAPISharingSession::ConnectToClient
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPISharingSession2.ConnectToClient
 - IRDPSRAPISharingSession.ConnectToClient
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPISharingSession::ConnectToClient


## -description


Used for reverse connect mode, where the sharer  connects to the viewer. In this mode, the sharer sends the invitation file to the viewer out-of-band by using  instant messaging (IM) or email. For the sharer to connect to the viewer, the sharer receives a connection string from the viewer out-of-band through IM or email.


## -parameters




### -param bstrConnectionString [in]

Type: <b>BSTR</b>

Connection string that the viewer sends to the sharer out-of-band through IM or email.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>



<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 

