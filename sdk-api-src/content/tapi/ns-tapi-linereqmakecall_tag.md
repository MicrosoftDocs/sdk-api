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

# linereqmakecall_tag structure


## -description


The 
<b>LINEREQMAKECALL</b> structure describes a request initiated by a call to the 
<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a> function.


## -struct-fields




### -field szDestAddress

<b>Null</b>-terminated destination address of the make-call request. The address can use the canonical address format or the dialable address format. The maximum length of the address is TAPIMAXDESTADDRESSSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.


### -field szAppName

<b>Null</b>-terminated user-friendly application name or filename of the application that originated the request. The maximum length of the address is TAPIMAXAPPNAMESIZE characters, which includes the <b>NULL</b> terminator.


### -field szCalledParty

<b>Null</b>-terminated user-friendly called-party name. The maximum length of the called-party information is TAPIMAXCALLEDPARTYSIZE characters, which includes the <b>NULL</b> terminator.


### -field szComment

<b>Null</b>-terminated comment about the call request. The maximum length of the comment string is TAPIMAXCOMMENTSIZE characters, which includes the <b>NULL</b> terminator.


## -remarks



This structure may not be extended.

The <b>szDestAddress</b> member contains the address of the remote party; the other members are useful for logging purposes. An application must use this structure to interpret the request buffer it received from 
<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a> with the LINEREQUESTMODE_MAKECALL request mode.




## -see-also




<a href="https://msdn.microsoft.com/c72ed61f-abbe-4a6d-9f8d-95afbd5dfb04">lineGetRequest</a>
 

 

