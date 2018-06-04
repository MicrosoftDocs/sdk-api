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

# _EAP_INTERACTIVE_UI_DATA_TYPE enumeration


## -description


The <b>EAP_INTERACTIVE_UI_DATA_TYPE</b> enumeration specifies the set of types of interactive UI context data supplied to certain supplicant API calls.


## -enum-fields




### -field EapCredReq

The data contains an EAP security credential retry request.


### -field EapCredResp

The data contains an EAP security credential retry response.


### -field EapCredExpiryReq

The data contains an EAP security credential expiration request.


### -field EapCredExpiryResp

The data contains an EAP security credential expiration response.


### -field EapCredLogonReq

The data contains an EAP security credential logon request.


### -field EapCredLogonResp

The data contains an EAP security credential logon response.


## -remarks



The <b>EAP_INTERACTIVE_UI_DATA_TYPE</b> is used to support Single-Sign-On (SSO).




## -see-also




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

