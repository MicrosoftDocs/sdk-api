---
UID: NF:objidl.IServerSecurity.QueryBlanket
title: IServerSecurity::QueryBlanket
author: windows-sdk-content
description: Retrieves information about the client that invoked one of the server's methods.
old-location: com\iserversecurity_queryblanket.htm
old-project: com
ms.assetid: 1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IServerSecurity interface [COM],QueryBlanket method, IServerSecurity.QueryBlanket, IServerSecurity::QueryBlanket, QueryBlanket, QueryBlanket method [COM], QueryBlanket method [COM],IServerSecurity interface, _com_iserversecurity_queryblanket, com.iserversecurity_queryblanket, objidlbase/IServerSecurity::QueryBlanket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IServerSecurity.QueryBlanket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IServerSecurity::QueryBlanket


## -description


Retrieves information about the client that invoked one of the server's methods.


## -parameters




### -param pAuthnSvc [out]

A pointer to the current authentication service. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">authentication service constants</a>. If the caller specifies <b>NULL</b>, the current authentication service is not retrieved.


### -param pAuthzSvc [out]

A pointer to a variable that receives the current authorization service. This will be a single value from the list of <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.


### -param pServerPrincName [out]

The current principal name. The string will be allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. By default, Schannel principal names will be in the msstd form. The fullsic form will be returned if EOAC_MAKE_FULLSIC is specified in the <i>pCapabilities</i> parameter. For more information on the msstd and fullsic forms, see <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.


### -param pAuthnLevel [out]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.


### -param pImpLevel [out]

This parameter must be <b>NULL</b>.


### -param pPrivs [out]

The privilege information for the client application. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. The information is only valid for the duration of the current call. For NTLMSSP, and Kerberos, this is a <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="https://msdn.microsoft.com/6b95bce8-5613-4403-9bda-16262596bb1b">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. For Schannel, this is a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the client's certificate. If the client has no certificate, <b>NULL</b> is returned. If the caller specifies <b>NULL</b>, the current privilege information is not retrieved.


### -param pCapabilities [in, out]

The capabilities of the call. To request that the principal name be returned in fullsic form if Schannel is the authentication service, the caller can set the EOAC_MAKE_FULLSIC flag in this parameter. If the caller specifies <b>NULL</b>, the current capabilities are not retrieved.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<b>QueryBlanket</b> is used by the server to find out about the client that invoked one of its methods. To get a pointer to <a href="https://msdn.microsoft.com/aacef77c-7185-44ed-aa1a-465c6100a431">IServerSecurity</a> for the current call on the current thread, call <a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>, specifying IID_IServerSecurity. This interface pointer may only be used in the same apartment as the call for the duration of the call.




## -see-also




<a href="https://msdn.microsoft.com/58a2c121-c324-4c33-aaca-490b5a09738c">CoQueryClientBlanket</a>



<a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>



<a href="https://msdn.microsoft.com/aacef77c-7185-44ed-aa1a-465c6100a431">IServerSecurity</a>
 

 

