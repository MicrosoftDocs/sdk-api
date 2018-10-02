---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorInvokeConfigUI
title: EapMethodAuthenticatorInvokeConfigUI function
author: windows-sdk-content
description: Defines a function that raises the EAP method's connection configuration user interface dialog box on the client.
old-location: eaphost\eapmethodauthenticatorinvokeconfigui.htm
tech.root: EAPHost
ms.assetid: 6d3083a6-1bd2-4dbf-9f8d-1a6e465188af
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EapMethodAuthenticatorInvokeConfigUI, EapMethodAuthenticatorInvokeConfigUI function [EAPHost], eaphost.eapmethodauthenticatorinvokeconfigui, eapmethodauthenticatorapis/EapMethodAuthenticatorInvokeConfigUI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eapmethodauthenticatorapis.h
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
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorInvokeConfigUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapMethodAuthenticatorInvokeConfigUI function


## -description


Defines a function that raises the EAP method's connection configuration user interface dialog box on the client.

<b>EapMethodAuthenticatorInvokeConfigUI</b> is a function prototype.

<b>EapHostAuthenticatorInvokeConfigUI</b> must be called on threads that have COM initialized for <a href="Http://go.microsoft.com/fwlink/p/?linkid=83881">Single Threaded Apartment</a>. This can be achieved by calling COM API <a href="_com_CoInitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="_com_CoUninitialize">CoUninitialize</a> must be called before exiting.


## -parameters




### -param pEapMethodType [in]

A pointer to an <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param hwndParent [in]

A handle to the parent window which will launch the connection configuration user interface dialog box.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param pwszMachineName [in]

The name of the target machine being configured. <b>NULL</b> means that the local machine is being configured.


### -param dwSizeOfConfigIn [in]

Specifies the size, in bytes, of <i>pConfigIn</i>. May be set to 0.


### -param pConfigIn [in]

A pointer to a byte buffer that contains configuration elements. The buffer is of size <i>dwSizeOfConfigIn</i>. This parameter can be <b>NULL</b> if <i>dwSizeOfConfigIn</i> is set to 0. 



### -param pdwSizeOfConfigOut [out]

Specifies the size, in bytes, of the configuration data returned in <i>ppConfigOut</i>.


### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains updated configuration data from the user. After consuming the data, this memory must be freed by calling <a href="https://msdn.microsoft.com/9ec9f468-4589-4832-9f17-ddc0b64b88f1">EapMethodAuthenticatorFreeMemory</a>.


### -param ppEapError [out]

A pointer to the affdress of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/8fcf82d6-9809-4a28-a694-1f7494216f82">EapMethodAuthenticatorFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/319516ee-b21d-4375-8c90-e3abe0a457e8">EAPHost Authenticator Method Functions</a>
 

 

