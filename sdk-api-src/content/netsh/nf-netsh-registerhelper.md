---
UID: NF:netsh.RegisterHelper
title: RegisterHelper function
author: windows-sdk-content
description: Is called from within a helper's exposed InitHelperDll function, and registers the helper with the NetShell context.
old-location: netshell\registerhelper.htm
old-project: NetShell
ms.assetid: 9c9ac64a-6edd-4348-80c7-4192726e5108
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: RegisterHelper, RegisterHelper function [NetShell], _netsh_registerhelper, netsh/RegisterHelper, netshell.registerhelper
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NS_REQS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - RegisterHelper
product: Windows
targetos: Windows
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RegisterHelper function


## -description


The 
<b>RegisterHelper</b> function is called from within a helper's exposed 
<a href="https://msdn.microsoft.com/9af7e818-bb08-4d35-bab4-43cb94845f25">InitHelperDll</a> function, and registers the helper with the NetShell context.


## -parameters




### -param pguidParentContext [in]

A pointer to GUID of another helper under which the helper should be installed. If null, the helper is installed as a top-level helper.


### -param pfnRegisterSubContext [in]

Attributes of the helper.


## -see-also




<a href="https://msdn.microsoft.com/9af7e818-bb08-4d35-bab4-43cb94845f25">InitHelperDll</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 

