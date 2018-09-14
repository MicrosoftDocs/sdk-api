---
UID: NF:eapmethodpeerapis.EapPeerSetCredentials
title: EapPeerSetCredentials function
author: windows-sdk-content
description: Supplies new or updated authentication credentials to the EAP method.
old-location: eaphost\eappeersetcredentials.htm
tech.root: EAPHost
ms.assetid: d50a72bd-0b3f-4b68-be96-5debb3fd99f8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapPeerSetCredentials, EapPeerSetCredentials function [EAPHost], eaphost.eappeersetcredentials, eapmethodpeerapis/EapPeerSetCredentials
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EapPeerSetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerSetCredentials function


## -description


Supplies new or updated authentication credentials to the EAP method. 


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSION_HANDLE</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionHandle</i> parameter in a previous call to <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a>.


### -param pwszIdentity [in]

A pointer that specifies the user identity for which to set the credentials. This user identity string is obtained by calling the <a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a> function.


### -param pwszPassword [in]

A pointer that contains the clear text password for the user identity.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



If the registry key <b>InvokeUserNameDlg</b>  is set, <i>EapPeerSetCredentials</i> should be exported. If the registry key <b>InvokeUserNameDlg</b>  is not set, <i>EapPeerSetCredentials</i> should export the <a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a> and <a href="https://msdn.microsoft.com/9b3a525a-2322-496e-83c7-a3180235583a">EapPeerInvokeIdentityUI</a> functions.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>



<a href="https://msdn.microsoft.com/24ae093f-5ddf-4b09-934f-d0e945335cde">EapPeerGetIdentity</a>



<a href="https://msdn.microsoft.com/9b3a525a-2322-496e-83c7-a3180235583a">EapPeerInvokeIdentityUI</a>



<a href="https://msdn.microsoft.com/d50a72bd-0b3f-4b68-be96-5debb3fd99f8">EapPeerSetCredentials</a>
 

 

