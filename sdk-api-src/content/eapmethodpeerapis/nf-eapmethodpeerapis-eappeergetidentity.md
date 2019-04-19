---
UID: NF:eapmethodpeerapis.EapPeerGetIdentity
title: EapPeerGetIdentity function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Returns the user data and user identity after being called by EAPHost.
old-location: eaphost\eappeergetidentity.htm
tech.root: eaphost
ms.assetid: 24ae093f-5ddf-4b09-934f-d0e945335cde
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerGetIdentity, EapPeerGetIdentity function [EAPHost], eaphost.eappeergetidentity, eapmethodpeerapis/EapPeerGetIdentity
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerGetIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerGetIdentity function


## -description


Returns the user data and user identity after being called by EAPHost.


## -parameters




### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwSizeofConnectionData [in]

Specifies the size, in bytes, of the connection data buffer provided in <i>pConnectionData</i>


### -param pConnectionData [in]

A pointer to a byte buffer that contains the opaque configuration data BLOB. 


### -param dwSizeofUserData [in]

Specifies the size, in bytes, of the user data buffer provided in <i>pUserData</i>.


### -param pUserData [in]

A pointer to the user data specific to this authentication used to   pre-populate the user data.
When this API is called for the first time, or when a new authentication session starts, this parameter is <b>NULL</b>.
Otherwise, set this parameter to the <b>pUserData</b> member of the structure pointed to by the<i>ppResult</i> parameter received by <b>EapPeerGetResult</b>. 
  


### -param hTokenImpersonateUser [in]

Specifies a handle to the impersonation token of the user being authenticated. This handle will be <b>NULL</b> when doing machine authentication. By using this handle an EAP method can impersonate the user for the purpose of obtaining user specific information such as user name, domain name and credentials.


### -param pfInvokeUI [out]

Returns <b>TRUE</b> if the user identity and user data blob aren't returned successfully, and the method seeks to collect the information from the user through the user interface dialog.


### -param pdwSizeOfUserDataOut [in, out]

Specifies the size, in bytes, of the <i>ppUserDataOut</i>buffer.


### -param ppUserDataOut [out]

A pointer to a pointer to the returned user data. The data is passed to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>   as input <i>pUserData</i>.


### -param ppwszIdentity [out]

 A pointer to the returned user identity. The pointer will be included in the identity response packet   and returned to the server.


### -param ppEapError [out]

A pointer to the pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/9b3a525a-2322-496e-83c7-a3180235583a">EapPeerInvokeIdentityUI</a>
 

 

