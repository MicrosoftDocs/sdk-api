---
UID: NF:eappapis.EapHostPeerSetResponseAttributes
title: EapHostPeerSetResponseAttributes function (eappapis.h)
author: windows-sdk-content
description: Provides updated EAP authentication attributes to EAPHost.
old-location: eaphost\eaphostpeersetresponseattributes.htm
tech.root: eaphost
ms.assetid: b8ce5510-f5ba-403c-8709-940ae58cd10d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerSetResponseAttributes, EapHostPeerSetResponseAttributes function [EAPHost], eaphost.eaphostpeersetresponseattributes, eappapis/EapHostPeerSetResponseAttributes
ms.topic: function
req.header: eappapis.h
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerSetResponseAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363575(v=VS.85).aspx">EapHostPeerResponseAction</a> enumeration value that specifies the action code for the next step the supplicant must take as a response.


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
 

 

