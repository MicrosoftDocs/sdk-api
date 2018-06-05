---
UID: NF:rdpencomapi.IRDPSRAPISharingSession2.SendControlLevelChangeResponse
title: IRDPSRAPISharingSession2::SendControlLevelChangeResponse
author: windows-sdk-content
description: Sends an OnControlLevelChangeResponse event.
old-location: rdp\irdpsrapisharingsession2_sendcontrollevelchangeresponse.htm
old-project: Rdp
ms.assetid: d10c8f2b-b1ee-4966-9e96-21e78124874b
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: IRDPSRAPISharingSession2 interface [RDP],SendControlLevelChangeResponse method, IRDPSRAPISharingSession2.SendControlLevelChangeResponse, IRDPSRAPISharingSession2::SendControlLevelChangeResponse, SendControlLevelChangeResponse, SendControlLevelChangeResponse method [RDP], SendControlLevelChangeResponse method [RDP],IRDPSRAPISharingSession2 interface, rdp.irdpsrapisharingsession2_sendcontrollevelchangeresponse, rdpencomapi/IRDPSRAPISharingSession2::SendControlLevelChangeResponse
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPSRAPISharingSession2.SendControlLevelChangeResponse
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRDPSRAPISharingSession2::SendControlLevelChangeResponse


## -description


Sends an <a href="https://msdn.microsoft.com/E190DAEC-776A-4248-8A73-073AB6F2FE8A">OnControlLevelChangeResponse</a> event.


## -parameters




### -param pAttendee [in]

Attendee that requests control.


### -param RequestedLevel [in]

Level of control requested by the attendee. For possible values, see the <a href="https://msdn.microsoft.com/f97b0493-82bf-487e-adc1-2dc40eeeb36c">CTRL_LEVEL</a> enumeration.


### -param ReasonCode [in]

Specifies the reason for the change.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 

