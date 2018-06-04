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

# _SCESVC_CALLBACK_INFO_ structure


## -description


The <b>SCESVC_CALLBACK_INFO</b> structure contains an opaque database handle and callback function pointers to query, set, and free information.


## -struct-fields




### -field sceHandle

Specifies the opaque handle passed to the attachment by the Security Configuration tool set. This handle is used by support functions to read information from and write information to the security database.


### -field pfQueryInfo

Pointer to a 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> callback function that queries information in the security database.


### -field pfSetInfo

Pointer to a 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> callback function that sets information in the security database.


### -field pfFreeInfo

Pointer to a 
<a href="https://msdn.microsoft.com/e7cafdbc-9ca2-4bb1-b8ed-d5553acaf7bc">PFSCE_FREE_INFO</a> callback function that frees information in the security database.


### -field pfLogInfo

Pointer to a 
<a href="https://msdn.microsoft.com/8960b0c0-abde-4ea1-bbe4-7409a848d81b">PFSCE_LOG_INFO</a> callback function that logs messages to the configuration log file or analysis log file.


## -see-also




<a href="https://msdn.microsoft.com/8db91e6f-b31e-40c6-a158-b4b3b00ba0c0">SCE_HANDLE</a>
 

 

