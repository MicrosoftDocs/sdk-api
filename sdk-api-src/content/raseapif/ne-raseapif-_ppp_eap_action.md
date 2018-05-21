---
UID: NE:raseapif._PPP_EAP_ACTION
title: "_PPP_EAP_ACTION"
author: windows-driver-content
description: The PPP_EAP_ACTION enumerated type specifies actions that the Connection Manager should take on behalf of the authentication protocol.
old-location: eap\ppp_eap_action.htm
old-project: EAP
ms.assetid: 5b1ead41-1fc0-41af-8614-3246d220c88d
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: EAPACTION_Authenticate, EAPACTION_Done, EAPACTION_IndicateIdentity, EAPACTION_IndicateTLV, EAPACTION_NoAction, EAPACTION_Send, EAPACTION_SendAndDone, EAPACTION_SendWithTimeout, EAPACTION_SendWithTimeoutInteractive, PPP_EAP_ACTION, PPP_EAP_ACTION enumeration [EAP], _PPP_EAP_ACTION, _eap_ppp_eap_action, eap.ppp_eap_action, raseapif/EAPACTION_Authenticate, raseapif/EAPACTION_Done, raseapif/EAPACTION_IndicateIdentity, raseapif/EAPACTION_IndicateTLV, raseapif/EAPACTION_NoAction, raseapif/EAPACTION_Send, raseapif/EAPACTION_SendAndDone, raseapif/EAPACTION_SendWithTimeout, raseapif/EAPACTION_SendWithTimeoutInteractive, raseapif/PPP_EAP_ACTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasPhonebookDlgW (Unicode) and RasPhonebookDlgA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PPP_EAP_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Raseapif.h
api_name:
-	PPP_EAP_ACTION
product: Windows
targetos: Windows
req.lib: Rasdlg.lib
req.dll: Rasdlg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

