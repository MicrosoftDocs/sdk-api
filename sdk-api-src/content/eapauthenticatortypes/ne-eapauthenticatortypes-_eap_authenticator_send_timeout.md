---
UID: NE:eapauthenticatortypes._EAP_AUTHENTICATOR_SEND_TIMEOUT
title: "_EAP_AUTHENTICATOR_SEND_TIMEOUT"
author: windows-sdk-content
description: Indicates to the authenticator method the amount of time to wait for user input after the packet is sent. The timeout value can be set to none.
old-location: eaphost\eap_authenticator_send_timeout.htm
old-project: eaphost
ms.assetid: 56c3da89-eaa8-4ea9-a912-3e15d713ba45
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EAP_AUTHENTICATOR_SEND_TIMEOUT, EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration [EAPHost], EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC, EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE, EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE, _EAP_AUTHENTICATOR_SEND_TIMEOUT, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE, eaphost.eap_authenticator_send_timeout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: eapauthenticatortypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EAP_AUTHENTICATOR_SEND_TIMEOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapAuthenticatorTypes.h
api_name:
 - EAP_AUTHENTICATOR_SEND_TIMEOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration


## -description


Indicates to the authenticator method the amount of time to wait for user input after the packet is sent. The timeout value can be set to none.


## -enum-fields




### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE

 Sends the packet and never times out; the user can enter a response at any time. 


### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC

Sends the packet and waits for a standard period of time for a response.


### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE

Sends the packet and waits for a response for a longer period of time to allow for an interactive session.


## -see-also




<a href="https://msdn.microsoft.com/8c21625f-a9b7-4ea5-98ff-cdcce637dad8">EAPHost Authenticator Method Enumerations</a>
 

 

