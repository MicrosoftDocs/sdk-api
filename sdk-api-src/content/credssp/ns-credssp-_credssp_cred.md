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

# _CREDSSP_CRED structure


## -description


 The <b>CREDSSP_CRED</b> structure specifies authentication data for both Schannel and Negotiate <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a>.


## -struct-fields




### -field Type

The <a href="https://msdn.microsoft.com/d30e219b-ea39-41da-b714-3ceb13a5614d">CREDSPP_SUBMIT_TYPE</a> enumeration value that specifies the type of credentials contained in this structure.


### -field pSchannelCred

A pointer to a set of Schannel credentials.


### -field pSpnegoCred

A pointer to a set of Negotiate credentials.


## -see-also




<a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle (CredSSP)</a>



<a href="https://msdn.microsoft.com/d30e219b-ea39-41da-b714-3ceb13a5614d">CREDSPP_SUBMIT_TYPE</a>
 

 

