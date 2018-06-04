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

# _EAP_CONFIG_INPUT_FIELD_TYPE enumeration


## -description


 The <b>EAP_CONFIG_INPUT_FIELD_TYPE</b> enumeration defines a set of possible  input field types available when querying for user credentials.


## -enum-fields




### -field EapConfigInputUsername

The input field contains a user's application logon name.


### -field EapConfigInputPassword

The input field contains a user's application logon password.


### -field EapConfigInputNetworkUsername

The input field contains a user's network logon name. This is used as an alternate logon user name for <b>EapConfigInputUsername</b>.


### -field EapConfigInputNetworkPassword

The input field contains a user's network login password. This is used as an alternate logon password for <b>EapConfigInputPassword</b>.


### -field EapConfigInputPin

The input field contains the user's network access PIN.


### -field EapConfigInputPSK

The input field contains the user's Flexible Authentication via Secure Tunneling (EAP-FAST) Pre-Shared Key(PSK).


### -field EapConfigInputEdit

The input field contains a generic logon token string.


### -field EapConfigSmartCardUsername

Windows 7 or later: The input field contains the username from a  smartcard certificate.


### -field EapConfigSmartCardError

Windows 7 or later: If an authentication using a smartcard did not succeed in the previous attempt of the current session, this input field contains an error message citing the failure reason.


## -remarks



The <b>EAP_CONFIG_INPUT_FIELD_TYPE</b> enumeration can be employed to support Single-Sign-On (SSO).




## -see-also




<a href="https://msdn.microsoft.com/2bf991f2-44b8-4815-b6c7-582f51087c83">Common EAPHost API Enumerations</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

