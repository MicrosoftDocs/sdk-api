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

# EapHostPeerSetResponseAttributes function


## -description


Provides updated EAP authentication attributes to EAPHost.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param pAttribs [in]

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseAction</a> enumeration value that specifies the action code for the next step the supplicant must take as a response.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -remarks



To progress to the next step in the state machine after a call to <a href="https://msdn.microsoft.com/84df4877-9ac9-4ab5-a357-276880051ff0">EapHostPeerGetResponseAttributes</a>, the supplicant must call <b>EapHostPeerSetResponseAttributes</b>. The supplicant must do so to pass a valid <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EapAttributes</a>  structure, even if the supplicant cannot use the attributes
returned from <b>EapHostPeerGetResponseAttributes</b>.   

The following example shows a  <b>EapHostPeerSetResponseAttributes</b> call that is made solely to progress to the next state in the state machine. 

<pre class="syntax" xml:space="preserve"><code>EapHostPeerGetResponseAttributes(session_id, &amp;eapAttributes, ppEapError);

// overwrite attributes returned by EapHostPeerGetResponseAttributes
EapAttributes eapAttributes={0,NULL};

// progress to the next state in the state machine
EapHostPeerSetResponseAttributes(session_id, &amp;eapAttributes, pEapOutput, ppEapError);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/84df4877-9ac9-4ab5-a357-276880051ff0">EapHostPeerGetResponseAttributes</a>
 

 

