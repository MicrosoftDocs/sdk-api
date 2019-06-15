---
UID: NE:raseapif._PPP_EAP_ACTION
title: PPP_EAP_ACTION (raseapif.h)
author: windows-sdk-content
description: The PPP_EAP_ACTION enumerated type specifies actions that the Connection Manager should take on behalf of the authentication protocol.
old-location: eap\ppp_eap_action.htm
tech.root: EAP
ms.assetid: 5b1ead41-1fc0-41af-8614-3246d220c88d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAPACTION_Authenticate, EAPACTION_Done, EAPACTION_IndicateIdentity, EAPACTION_IndicateTLV, EAPACTION_NoAction, EAPACTION_Send, EAPACTION_SendAndDone, EAPACTION_SendWithTimeout, EAPACTION_SendWithTimeoutInteractive, PPP_EAP_ACTION, PPP_EAP_ACTION enumeration [EAP], _eap_ppp_eap_action, eap.ppp_eap_action, raseapif/EAPACTION_Authenticate, raseapif/EAPACTION_Done, raseapif/EAPACTION_IndicateIdentity, raseapif/EAPACTION_IndicateTLV, raseapif/EAPACTION_NoAction, raseapif/EAPACTION_Send, raseapif/EAPACTION_SendAndDone, raseapif/EAPACTION_SendWithTimeout, raseapif/EAPACTION_SendWithTimeoutInteractive, raseapif/PPP_EAP_ACTION
ms.topic: enum
f1_keywords: ["raseapif/PPP_EAP_ACTION"]
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - PPP_EAP_ACTION
product: Windows
targetos: Windows
req.typenames: PPP_EAP_ACTION
req.redist: 
ms.custom: 19H1
---

# PPP_EAP_ACTION enumeration


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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/raseapif/ns-raseapif-_ppp_eap_output">PPP_EAP_OUTPUT</a> structure is set with an appropriate value.


### -field EAPACTION_SendAndDone

Directs the Connection Manager to send a message (without a time out), then end the authentication session. <b>EAPACTION_SendAndDone</b> indicates that the <b>dwAuthResultCode</b> member of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/raseapif/ns-raseapif-_ppp_eap_output">PPP_EAP_OUTPUT</a> structure is set with an appropriate value.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eap/eap-enumerations">EAP Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference">Extensible Authentication Protocol Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/raseapif/ns-raseapif-_ppp_eap_input">PPP_EAP_INPUT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/raseapif/ns-raseapif-_ppp_eap_output">PPP_EAP_OUTPUT</a>
 

 

