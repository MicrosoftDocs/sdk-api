---
UID: NS:objidl.tagSOLE_AUTHENTICATION_INFO
title: tagSOLE_AUTHENTICATION_INFO
author: windows-sdk-content
description: Identifies an authentication service, authorization service, and the authentication information for the specified authentication service.
old-location: com\sole_authentication_info.htm
old-project: com
ms.assetid: 23beb1b1-e4b7-4282-9868-5caf40a69a61
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSOLE_AUTHENTICATION_INFO, PSOLE_AUTHENTICATION_INFO, PSOLE_AUTHENTICATION_INFO structure pointer [COM], SOLE_AUTHENTICATION_INFO, SOLE_AUTHENTICATION_INFO structure [COM], _com_SOLE_AUTHENTICATION_INFO, com.sole_authentication_info, objidlbase/PSOLE_AUTHENTICATION_INFO, objidlbase/SOLE_AUTHENTICATION_INFO, tagSOLE_AUTHENTICATION_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: Objidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SOLE_AUTHENTICATION_INFO, *PSOLE_AUTHENTICATION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - SOLE_AUTHENTICATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagSOLE_AUTHENTICATION_INFO structure


## -description


Identifies an authentication service, authorization service, and the authentication information for the specified authentication service.


## -struct-fields




### -field dwAuthnSvc

The authentication service. This member can be a single value from the <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">Authentication Service Constants</a>.


### -field dwAuthzSvc

The authorization service. This member can be a single value from the <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">Authorization Constants</a>.


### -field pAuthInfo

A pointer to the authentication information, whose type is specific to the authentication service identified by <b>dwAuthnSvc</b>.

For Schannel (<a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">RPC_C_AUTHN_GSS_SCHANNEL</a>), this member either points to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the client's X.509 certificate or is <b>NULL</b> if the client has no certificate or wishes to remain anonymous to the server.

For NTLMSSP (<a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">RPC_C_AUTHN_WINNT</a>) and Kerberos (RPC_C_AUTHN_GSS_KERBEROS), this member points to a <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="https://msdn.microsoft.com/6b95bce8-5613-4403-9bda-16262596bb1b">SEC_WINNT_AUTH_IDENTITY_EX</a> structure that contains the user name and password.

For Snego (<a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">RPC_C_AUTHN_GSS_NEGOTIATE</a>), this member is either <b>NULL</b>, points to a <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> structure, or points to a <a href="https://msdn.microsoft.com/6b95bce8-5613-4403-9bda-16262596bb1b">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If it is <b>NULL</b>, Snego will pick a list of authentication services based on those available on the client computer. If it points to a <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure, the structure's <b>PackageList</b> member must point to a string containing a comma-separated list of authentication service names and the <b>PackageListLength</b> member must give the number of bytes in the <b>PackageList</b> string. If <b>PackageList</b> is <b>NULL</b>, all calls using Snego will fail.

For authentication services not registered with DCOM, <b>pAuthInfo</b> must be set to <b>NULL</b> and DCOM will use the process identity to represent the client. For more information, see <a href="https://msdn.microsoft.com/a0c095a8-93b7-4350-aac6-a9a066cccffd">COM and Security Packages</a>.


## -see-also




<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>



<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/21f7aef3-b6be-41cc-a6ed-16d3778e3cee">SOLE_AUTHENTICATION_LIST</a>
 

 

