---
UID: NF:netsh.RegisterHelper
title: RegisterHelper function (netsh.h)
description: Is called from within a helper's exposed InitHelperDll function, and registers the helper with the NetShell context.
helpviewer_keywords: ["RegisterHelper","RegisterHelper function [NetShell]","_netsh_registerhelper","netsh/RegisterHelper","netshell.registerhelper"]
old-location: netshell\registerhelper.htm
tech.root: netshell
ms.assetid: 9c9ac64a-6edd-4348-80c7-4192726e5108
ms.date: 12/05/2018
ms.keywords: RegisterHelper, RegisterHelper function [NetShell], _netsh_registerhelper, netsh/RegisterHelper, netshell.registerhelper
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterHelper
 - netsh/RegisterHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - RegisterHelper
---

# RegisterHelper function


## -description

The 
<b>RegisterHelper</b> function is called from within a helper's exposed 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_dll_init_fn">InitHelperDll</a> function, and registers the helper with the NetShell context.

## -parameters

### -param pguidParentContext [in]

A pointer to GUID of another helper under which the helper should be installed. If null, the helper is installed as a top-level helper.

### -param pfnRegisterSubContext [in]

Attributes of the helper.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_dll_init_fn">InitHelperDll</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>