---
UID: NF:eappapis.EapHostPeerGetIdentity
title: EapHostPeerGetIdentity function
author: windows-sdk-content
description: This function is called by tunnel methods to request identity information from the inner methods. This function returns the identity and user credential information.
old-location: eaphost\eaphostpeergetidentity.htm
tech.root: eaphost
ms.assetid: 25d1b360-694d-4ab8-9be4-a79354367068
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapHostPeerGetIdentity, EapHostPeerGetIdentity function [EAPHost], eaphost.eaphostpeergetidentity, eappapis/EapHostPeerGetIdentity
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.dll: Eapphost.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eapphost.dll
api_name:
 - EapHostPeerGetIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerGetIdentity function


## -description


This function is called by tunnel methods to request identity information from the inner methods. This function returns the identity and user credential information.


## -parameters




### -param dwVersion [in]

The version number of the API. Must be set to zero.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.


### -param dwSizeofConnectionData [in]

Size of the buffer indicated by the <i>pConnectionData</i> parameter, in bytes.


### -param pConnectionData [in]

Pointer to configuration data that is used for the EAP method.


### -param dwSizeofUserData [in]

Size of the buffer indicated by the <i>pUserData</i> parameter, in bytes.


### -param pUserData [in]

Pointer to user credential information that pertains to this authentication session.


### -param hTokenImpersonateUser [in]

Impersonation token for a logged-on user to collect user-related information.


### -param pfInvokeUI [out]

Returns <b>TRUE</b> if the user identity and user data blob aren't returned successfully, and the method seeks to collect the information from the user through the user interface dialog.


### -param pdwSizeOfUserDataOut [in, out]

Size of the buffer indicated by the <i>ppUserDataOut</i> parameter, in bytes.


### -param ppUserDataOut [out]

User data information returned by the method. After use, this memory must be freed by calling <a href="https://msdn.microsoft.com/d27233a0-b41f-43f6-a934-1ab8df8b0581">EapHostPeerFreeRuntimeMemory</a>.


### -param ppwszIdentity [out]

A pointer to a NULL-terminated user identity string. After use, this memory must be freed by calling <a href="https://msdn.microsoft.com/d27233a0-b41f-43f6-a934-1ab8df8b0581">EapHostPeerFreeRuntimeMemory</a>.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


### -param ppvReserved [in, out]

Reserved for future use


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-Time Functions</a>



<a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>
 

 

