---
UID: NF:netsh.RegisterContext
title: RegisterContext function
author: windows-driver-content
description: Registers a helper context with NetShell.
old-location: netshell\registercontext.htm
old-project: NetShell
ms.assetid: 52cebe62-d4b6-4229-8418-c0ae9849822b
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: RegisterContext, RegisterContext function [NetShell], _netsh_registercontext, netsh/RegisterContext, netshell.registercontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NS_REQS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netsh.exe
api_name:
-	RegisterContext
product: Windows
targetos: Windows
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RegisterContext function


## -description


The 
<b>RegisterContext</b> function registers a helper context with NetShell. The 
<b>RegisterContext</b> function should be called from the 
<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a> entry point (the start function) passed to the 
<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a> function in the <b>pfnStart</b> member of the 
<a href="https://msdn.microsoft.com/5041801d-384d-4faf-b0df-2a76b083facd">NS_CONTEXT_ATTRIBUTES</a> structure passed in its <i>pChildAttributes</i> parameter.


## -parameters




### -param pChildContext [in]

Attributes of the context to register.


## -remarks



For top-level helpers, the 
<b>RegisterContext</b> parameter passed during the course of its initialization function is a pointer to the 
<b>RegisterContext</b> function. The pointer should be cast to type <b>NS_REGISTER_CONTEXT</b> before use.




## -see-also




<a href="https://msdn.microsoft.com/5041801d-384d-4faf-b0df-2a76b083facd">NS_CONTEXT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a>



<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a>
 

 

