---
UID: NS:sspi._SecPkgContext_ClientSpecifiedTarget
title: SecPkgContext_ClientSpecifiedTarget (sspi.h)
author: windows-sdk-content
description: Specifies the service principal name (SPN) of the initial target when calling the QueryContextAttributes (Digest) function.
old-location: security\secpkgcontext_clientspecifiedtarget.htm
tech.root: SecAuthN
ms.assetid: 67536f69-a1fc-4f26-84dc-872635bafa3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget structure pointer [Security], SecPkgContext_ClientSpecifiedTarget, SecPkgContext_ClientSpecifiedTarget structure [Security], security.secpkgcontext_clientspecifiedtarget, sspi/PSecPkgContext_ClientSpecifiedTarget, sspi/SecPkgContext_ClientSpecifiedTarget"
ms.topic: struct
req.header: sspi.h
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
 - Sspi.h
api_name:
 - SecPkgContext_ClientSpecifiedTarget
product: Windows
targetos: Windows
req.typenames: SecPkgContext_ClientSpecifiedTarget, *PSecPkgContext_ClientSpecifiedTarget
req.redist: 
---

# SecPkgContext_ClientSpecifiedTarget structure


## -description


The <b>SecPkgContext_ClientSpecifiedTarget</b> structure specifies the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">service principal name</a> (SPN) of the initial target when calling the <a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a> function.


## -struct-fields




### -field sTargetName

The SPN of the initial target.


## -see-also




<a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a>
 

 

