---
UID: NS:webservices._WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
title: "_WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL"
author: windows-sdk-content
description: Type for supplying a Windows Integrated Authentication credential based on the current Windows identity.
old-location: wsw\ws_default_windows_integrated_auth_credential.htm
tech.root: wsw
ms.assetid: 14753a2d-6054-4041-a72b-4cd7a9576f3b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows], _WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, webservices/WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, wsw.ws_default_windows_integrated_auth_credential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
product: Windows
targetos: Windows
req.typenames: WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
req.redist: 
---

# _WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description


Type for supplying a Windows Integrated Authentication credential based on the current Windows identity. If this credential subtype is used for a security binding, the current thread token on the thread that calls <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> or <a href="https://msdn.microsoft.com/b8a0afc7-2004-419d-8ab2-ce197c7e396d">WsOpenServiceProxy</a> is used as the Windows identity when sending messages or making service calls.


<a href="https://msdn.microsoft.com/e18e0005-89bd-435e-9a12-6602c3c638b7">WsAcceptChannel</a> and <a href="https://msdn.microsoft.com/4e6ef553-7f0e-4ed7-bbdd-e85d4e0a095c">WsOpenServiceHost</a> do not support this credential type when called from an impersonating thread. 


This type derives from the base type <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>. For an instance of this type, the type selector field <b>credential.credentialType</b> must have the value <b>WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL_TYPE</b>. 




## -struct-fields




### -field credential

The base type from which this type and all other Windows Integrated Authentication credential types derive.
                See <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>.

