---
UID: NF:eapmethodpeerapis.EapPeerInvokeIdentityUI
title: EapPeerInvokeIdentityUI function
author: windows-sdk-content
description: Raises a custom interactive user interface dialog to obtain user identity information for the EAP method on the client.
old-location: eaphost\eappeerinvokeidentityui.htm
old-project: EAPHost
ms.assetid: 9b3a525a-2322-496e-83c7-a3180235583a
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapPeerInvokeIdentityUI, EapPeerInvokeIdentityUI function [EAPHost], eaphost.eappeerinvokeidentityui, eapmethodpeerapis/EapPeerInvokeIdentityUI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eapmethodpeerapis.h
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
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	eapmethodpeerapis.h
api_name:
-	EapPeerInvokeIdentityUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerInvokeIdentityUI function


## -description


Raises a custom interactive user interface dialog to obtain user identity information for the EAP method on the client.


## -parameters




### -param pEapType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param dwFlags

TBD


### -param hwndParent [in]

A handle to the parent window which will spawn the interactive user interface dialog to obtain the identity data.


### -param dwSizeOfConnectionData [in]

The size, in bytes, of the user interface context data specified by <i>pUIContextData</i>.


### -param pConnectionData [in]

A pointer to an opaque byte buffer that contains the connection data.


### -param dwSizeOfUserData [out]

Specifies the size, in bytes, of the user identity data returned in <i>dwSizeOfUserData</i>.


### -param pUserData [in]

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the<i>ppResult</i> parameter received by <b>EapPeerGetResult</b>. 


### -param pdwSizeOfUserDataOut [out]

Specifies the size, in bytes, of the <i>ppUserDataOut</i>
buffer.


### -param ppUserDataOut [out]

A pointer to the pointer of the returned user data. The data is passed to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>   as input <i>pUserData</i>.


### -param ppwszIdentity [out]

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


#### - dwflags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/ba5c90b2-5185-4810-84a2-d08e62e8105c">EAPHost Peer Method Configuration Functions</a>



<a href="https://msdn.microsoft.com/9b3a525a-2322-496e-83c7-a3180235583a">EapPeerInvokeIdentityUI</a>
 

 

