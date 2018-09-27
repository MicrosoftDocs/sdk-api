---
UID: NF:sspi.InitSecurityInterfaceA
title: InitSecurityInterfaceA function
author: windows-sdk-content
description: The InitSecurityInterface function returns a pointer to an SSPI dispatch table. This function enables clients to use SSPI without binding directly to an implementation of the interface.
old-location: security\initsecurityinterface.htm
tech.root: secauthn
ms.assetid: 1026eeab-e2d6-45f2-9677-82d6cfbf4e12
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: InitSecurityInterface, InitSecurityInterface function [Security], InitSecurityInterfaceA, InitSecurityInterfaceW, _ssp_initsecurityinterface, security.initsecurityinterface, sspi/InitSecurityInterface, sspi/InitSecurityInterfaceA, sspi/InitSecurityInterfaceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InitSecurityInterfaceW (Unicode) and InitSecurityInterfaceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
 - security.dll
 - schannel.dll
api_name:
 - InitSecurityInterface
 - InitSecurityInterfaceA
 - InitSecurityInterfaceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitSecurityInterfaceA function


## -description


The <b>InitSecurityInterface</b> function returns a pointer to an SSPI dispatch table. This function enables clients to use SSPI without binding directly to an implementation of the interface.


## -parameters






## -returns



If the function succeeds, the return value is a pointer to a 
<a href="https://msdn.microsoft.com/6315e8d6-b40a-4dd6-b6a6-598a965f93dc">SecurityFunctionTable</a> structure.

If the function fails, the return value is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/6315e8d6-b40a-4dd6-b6a6-598a965f93dc">SecurityFunctionTable</a>
 

 

