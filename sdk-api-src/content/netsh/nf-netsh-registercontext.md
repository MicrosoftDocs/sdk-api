---
UID: NF:netsh.RegisterContext
title: RegisterContext function (netsh.h)
author: windows-sdk-content
description: Registers a helper context with NetShell.
old-location: netshell\registercontext.htm
tech.root: netshell
ms.assetid: 52cebe62-d4b6-4229-8418-c0ae9849822b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegisterContext, RegisterContext function [NetShell], _netsh_registercontext, netsh/RegisterContext, netshell.registercontext
ms.topic: function
f1_keywords:
- netsh/RegisterContext
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
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Netsh.exe
api_name:
- RegisterContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterContext function


## -description


The 
<b>RegisterContext</b> function registers a helper context with NetShell. The 
<b>RegisterContext</b> function should be called from the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_start_fn">NS_HELPER_START_FN</a> entry point (the start function) passed to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nf-netsh-registerhelper">RegisterHelper</a> function in the <b>pfnStart</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/netsh/ns-netsh-ns_context_attributes">NS_CONTEXT_ATTRIBUTES</a> structure passed in its <i>pChildAttributes</i> parameter.


## -parameters




### -param pChildContext [in]

Attributes of the context to register.


## -remarks



For top-level helpers, the 
<b>RegisterContext</b> parameter passed during the course of its initialization function is a pointer to the 
<b>RegisterContext</b> function. The pointer should be cast to type <b>NS_REGISTER_CONTEXT</b> before use.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netsh/ns-netsh-ns_context_attributes">NS_CONTEXT_ATTRIBUTES</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_start_fn">NS_HELPER_START_FN</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nf-netsh-registerhelper">RegisterHelper</a>
 

 

