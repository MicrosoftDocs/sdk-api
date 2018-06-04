---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CoImpersonateClient function


## -description


Enables the server to impersonate the client of the current call for the duration of the call.




## -parameters






## -returns



This function supports the standard return values, including S_OK.




## -remarks



This method allows the server to impersonate the client of the current call for the duration of the call. If you do not call CoRevertToSelf, COM reverts automatically for you. This function will fail unless the object is being called with RPC_C_AUTHN_LEVEL_CONNECT or higher authentication in effect (which is any authentication level except RPC_C_AUTHN_LEVEL_NONE). This function encapsulates the following sequence of common calls (error handling excluded):

<pre class="syntax" xml:space="preserve"><code>    CoGetCallContext(IID_IServerSecurity, (void**)&amp;pss);
    pss-&gt;ImpersonateClient();
    pss-&gt;Release();
</code></pre>
<b>CoImpersonateClient</b> encapsulates the process of getting a pointer to an instance of <a href="https://msdn.microsoft.com/aacef77c-7185-44ed-aa1a-465c6100a431">IServerSecurity</a> that contains data about the current call, calling its <a href="https://msdn.microsoft.com/20398b63-0fcb-40ab-93ed-f4c75760eb9e">ImpersonateClient</a> method, and then releasing the pointer. One call to <a href="https://msdn.microsoft.com/8061ddbe-ed21-47f7-9ac4-b3ec910ff89d">CoRevertToSelf</a> (or <a href="https://msdn.microsoft.com/21952f54-439e-446f-a206-4b35759b1090">IServerSecurity::RevertToSelf</a>) will undo any number of  calls to impersonate the client.




## -see-also




<a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a>



<a href="https://msdn.microsoft.com/20398b63-0fcb-40ab-93ed-f4c75760eb9e">IServerSecurity::ImpersonateClient</a>



<a href="https://msdn.microsoft.com/b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b">Impersonation</a>



<a href="https://msdn.microsoft.com/7eaa0a66-7a80-4831-b0b6-b8eff4abd036">Impersonation and Asynchronous Calls</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

