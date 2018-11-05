---
UID: NF:objidlbase.IServerSecurity.ImpersonateClient
title: IServerSecurity::ImpersonateClient
author: windows-sdk-content
description: Enables a server to impersonate a client for the duration of a call.
old-location: com\iserversecurity_impersonateclient.htm
tech.root: com
ms.assetid: 20398b63-0fcb-40ab-93ed-f4c75760eb9e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IServerSecurity interface [COM],ImpersonateClient method, IServerSecurity.ImpersonateClient, IServerSecurity::ImpersonateClient, ImpersonateClient, ImpersonateClient method [COM], ImpersonateClient method [COM],IServerSecurity interface, _com_iserversecurity_impersonateclient, com.iserversecurity_impersonateclient, objidlbase/IServerSecurity::ImpersonateClient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IServerSecurity.ImpersonateClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServerSecurity::ImpersonateClient


## -description


Enables a server to impersonate a client for the duration of a call.


## -parameters






## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



Usually, a method executes on a thread that uses the access token of the process. However, when impersonating a client, the server runs in the client's security context so that the server has access to the resources that the client has access to. When impersonation is necessary, the server calls the <b>ImpersonateClient</b> method to cause an access token representing the client's credentials to be assigned to the current thread. This thread token is used for access checks. <a href="https://msdn.microsoft.com/21952f54-439e-446f-a206-4b35759b1090">RevertToSelf</a> restores the current thread's access token.

What the server can do on behalf of the client depends on the impersonation level set by the client, which is specified using one of the <a href="https://msdn.microsoft.com/ea5a3b46-b607-4192-a3cc-b2ec55ca94a6">impersonation level constants</a>. The server may impersonate the client on an encrypted call at identify, impersonate, or delegate level. For information about these levels of impersonation, see <a href="https://msdn.microsoft.com/7539bbee-063f-4788-aece-7b70684826c8">Impersonation Levels</a>.

The identity presented to a server called during impersonation depends on the type of cloaking value, if any, that is set by the client. For more information, see <a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a>.

At the end of each method call, COM will call <a href="https://msdn.microsoft.com/21952f54-439e-446f-a206-4b35759b1090">RevertToSelf</a> if the application does not.

Traditionally, impersonation information is not nested â€“ the last call to any impersonation mechanism overrides any previous impersonation. However, in the apartment model, impersonation is maintained during nested calls. Thus if the server A receives a call from B, impersonates, calls C, receives a call from D, impersonates, reverts, and receives the reply from C, the impersonation token will be set back to B, not A.

For information on using impersonation with asynchronous calls, see <a href="https://msdn.microsoft.com/7eaa0a66-7a80-4831-b0b6-b8eff4abd036">Impersonation and Asynchronous Calls</a>. 





## -see-also




<a href="https://msdn.microsoft.com/a3cbfbbc-fc6f-4d1b-8460-1e3351cd32d7">CoImpersonateClient</a>



<a href="https://msdn.microsoft.com/aacef77c-7185-44ed-aa1a-465c6100a431">IServerSecurity</a>
 

 

