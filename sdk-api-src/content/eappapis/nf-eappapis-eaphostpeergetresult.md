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

# EapHostPeerGetResult function


## -description


Obtains the authentication result for the specified EAP authentication session.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param reason [in]

An <a href="https://msdn.microsoft.com/f43d2883-d23f-455b-bde0-244a88630d25">EapHostPeerMethodResultReason</a> enumeration value that specifies the reason code for the authentication result returned in <i>ppResult</i>.


### -param ppResult [out]

A pointer to a <a href="https://msdn.microsoft.com/f43d2883-d23f-455b-bde0-244a88630d25">EapHostPeerMethodResultReason</a> structure that contains the authentication results. EAPHost fills this structure with authentication related information defined in <a href="https://msdn.microsoft.com/376e5399-61c9-4927-ac68-8a1bb4bdc7db">EapHostPeerMethodResult</a>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. Supplicants must refer to this parameter to determine if the authentication was successful. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>. The return value does not indicate if the authentication was successful. Supplicants must refer to the <i>ppEapError</i> parameter to determine the authentication result.

If the function fails, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.




## -remarks



The supplicant calls <b>EapHostPeerGetResult</b> on completion of an authentication, which can occur in any of the following scenarios.
   

<ul>
<li>A call to <a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a> returned the <b>EapHostPeerResponseResult</b> action code.</li>
<li> The client timed out and wants to get the result based on the current
   state.</li>
<li> The supplicant received an alternate result, perhaps from a packet on the 
   lower layer.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a>
 

 

