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

# tapiRequestMakeCallA function


## -description


The 
<b>tapiRequestMakeCall</b> function requests the establishment of a voice call. A call-manager application is responsible for establishing the call on behalf of the requesting application, which is then controlled by the user's call-manager application.


## -parameters




### -param lpszDestAddress

Pointer to a memory location where the <b>null</b>-terminated destination address of the call request is located. The address can use the 
<a href="../tapi3/address_ovr.htm">canonical address</a> format. Validity of the specified address is not checked by this operation. The maximum length of the address is TAPIMAXDESTADDRESSSIZE characters, which includes the <b>NULL</b> terminator.


### -param lpszAppName

Pointer to a memory location where the <b>null</b>-terminated user-friendly application name of the call request is located. This pointer can be left <b>NULL</b> if the application does not supply an application name. The maximum length of the address is TAPIMAXAPPNAMESIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.


### -param lpszCalledParty

Pointer to a memory location where the <b>null</b>-terminated called party name for the called party of the call is located. This pointer can be left <b>NULL</b> if the application does not wish to supply this information. The maximum length of the string is TAPIMAXCALLEDPARTYSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.


### -param lpszComment

Pointer to a memory location where the <b>null</b>-terminated comment about the call is located. This pointer can be left <b>NULL</b> if the application does not supply a comment. The maximum length of the address is TAPIMAXCOMMENTSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible error return value are:

TAPIERR_NOREQUESTRECIPIENT, TAPIERR_INVALDESTADDRESS, TAPIERR_REQUESTQUEUEFULL, TAPIERR_INVALPOINTER.




## -remarks



A telephony-enabled application can request that a call be placed on its behalf by invoking 
<b>tapiRequestMakeCall</b>, providing only the destination address for the call. This request is forwarded to the user's call-control application, which places the call on behalf of the original application. A default call-control application is provided as part of  Telephony. Users can replace this with a call-control application of their choice.

Invoking 
<b>tapiRequestMakeCall</b> when no call control application is running returns the TAPIERR_NOREQUESTRECIPIENT error indication. If the call control application is not running, TAPI attempts to launch the highest-priority call control application (which is listed for <b>RequestMakeCall</b> in the registry). Invoking this function when the Assisted TAPI request queue is full returns the TAPIERR_REQUESTQUEUEFULL error.




## -see-also




<a href="https://msdn.microsoft.com/43ca86b0-0107-4937-b15a-47916e144527">Assisted Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

