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

# EAP_UI_DATA_FORMAT structure


## -description


The <b>EAP_UI_DATA_FORMAT</b> union specifies the value of the attribute stored in the <i>pbUiData</i> member of the <a href="https://msdn.microsoft.com/0b3cd58c-9396-4c79-842b-76bf03aa7d7a">EAP_INTERACTIVE_UI_DATA</a> structure. The structure of the <b>EAP_UI_DATA_FORMAT</b> union depends on the value of <i>dwDataType</i> as specified in <a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a>.


## -struct-fields




### -field credData

case(<i>EapCredReq</i>)

If <i>dwDataType</i> specifies a credential request type (<i>EapCredReq</i>), then the data pointed to by this parameter is defined by the <a href="https://msdn.microsoft.com/537a90fc-4dd2-44d4-93da-949f31130ac4">EAP_CRED_REQ </a>structure. 

 


case(<i>EapCredResp</i>)

If <i>dwDataType</i> specifies a credential response type (<i>EapCredResp</i>), then the data pointed to by this parameter is defined by the <a href="https://msdn.microsoft.com/714c75d8-71c7-4c3f-802a-a5e4f6ca65c2">EAP_CRED_RESP</a> structure


### -field credData.case

 


### -field credData.case.EapCredReq

 


### -field credData.case.EapCredResp

 


### -field credExpiryData

case(<i>eapCredExpiryReq</i>)

If <i>dwDataType</i> specifies a credential expiry request (<i>eapCredExpiryReq</i>), then the data pointed to by this parameter is defined by <a href="https://msdn.microsoft.com/baa2a580-0bfc-450a-9a96-f32d00127fa4">EAP_CRED_EXPIRY_REQ </a>structure.

case(<i>eapCredExpiryResp</i>)

If <i>dwDataType</i> specifies a credential expiry response type (<i>eapCredExpiryResp</i>), then this parameter is defined by <a href="https://msdn.microsoft.com/59b7f7d0-58af-4368-b3ea-6f180422a673">EAP_CRED_EXPIRY_RESP</a> structure


### -field credExpiryData.case

 


### -field credExpiryData.case.EapCredExpiryReq

 


### -field credExpiryData.case.EapCredExpiryResp

 


### -field credLogonData

case(<i>EapCredLogonReq</i>)

If <i>dwDataType</i> specifies a logon credential request type (<i>EapCredLogonReq</i>),  the data pointed to by this parameter is defined by the <a href="https://msdn.microsoft.com/1F1A2F77-054D-4FD2-83A5-69C3D77418B3">EAP_CRED_LOGON_REQ</a> structure. 


case(<i>EapCredLogonResp</i>)

If <i>dwDataType</i> specifies a logon credential response type (<i>EapCredLogonResp</i>), the data pointed to by this parameter is defined by the <a href="https://msdn.microsoft.com/1244A40F-6999-4053-97C4-1C4FB107B2F5">EAP_CRED_LOGON_RESP</a> structure



### -field credLogonData.case

 


### -field credLogonData.case.EapCredLogonReq

 


### -field credLogonData.case.EapCredLogonResp

 


### -field switch_type

 


### -field switch_type.EAP_INTERACTIVE_UI_DATA_TYPE

 




## -see-also




<a href="https://msdn.microsoft.com/baa2a580-0bfc-450a-9a96-f32d00127fa4">EAP_CRED_EXPIRY_REQ</a>



<a href="https://msdn.microsoft.com/59b7f7d0-58af-4368-b3ea-6f180422a673">EAP_CRED_EXPIRY_RESP</a>



<a href="https://msdn.microsoft.com/537a90fc-4dd2-44d4-93da-949f31130ac4">EAP_CRED_REQ</a>



<a href="https://msdn.microsoft.com/714c75d8-71c7-4c3f-802a-a5e4f6ca65c2">EAP_CRED_RESP</a>



<a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a>



<a href="https://msdn.microsoft.com/0b3cd58c-9396-4c79-842b-76bf03aa7d7a">EAP_INTERACTIVE_UI_DATA_TYPE</a>
 

 

