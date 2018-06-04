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

# _PPP_EAP_ACTION enumeration


## -description


The 
<b>PPP_EAP_ACTION</b> enumerated type specifies actions that the Connection Manager should take on behalf of the authentication protocol.


## -enum-fields




### -field EAPACTION_NoAction

Directs the Connection Manager to be passive.


### -field EAPACTION_Authenticate

Directs the Connection Manager to invoke the authentication provider to authenticate the user.


### -field EAPACTION_Done

Directs the Connection Manager Service to end the authentication session. <b>EAPACTION_Done</b> indicates that the <b>dwAuthResultCode</b> member of the 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> structure is set with an appropriate value.


### -field EAPACTION_SendAndDone

Directs the Connection Manager to send a message (without a time out), then end the authentication session. <b>EAPACTION_SendAndDone</b> indicates that the <b>dwAuthResultCode</b> member of the 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> structure is set with an appropriate value.


### -field EAPACTION_Send

Directs the Connection Manager to send a message without setting a time out to wait for a reply.


### -field EAPACTION_SendWithTimeout

Directs the Connection Manager to send a message and set a time out to wait for a reply.


### -field EAPACTION_SendWithTimeoutInteractive

Directs the Connection Manager to send a message and set a time out to wait for a reply, but instructs the Connection Manager not to increment the retry counter.


### -field EAPACTION_IndicateTLV

Reserved for system use.


### -field EAPACTION_IndicateIdentity

Reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/727398b3-7951-4393-b615-40ad90137fdc">EAP Enumerations</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a>



<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a>
 

 

