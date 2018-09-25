---
UID: NS:sspi._SecPkgContext_Sizes
title: "_SecPkgContext_Sizes"
author: windows-sdk-content
description: The SecPkgContext_Sizes structure indicates the sizes of important structures used in the message support functions. The QueryContextAttributes (General) function uses this structure.
old-location: security\secpkgcontext_sizes.htm
tech.root: secauthn
ms.assetid: 46b6a155-8855-4aa0-a513-aa5b3760fcd4
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PSecPkgContext_Sizes, PSecPkgContext_Sizes, PSecPkgContext_Sizes structure pointer [Security], SecPkgContext_Sizes, SecPkgContext_Sizes structure [Security], _SecPkgContext_Sizes, _ssp_secpkgcontext_sizes, security.secpkgcontext_sizes, sspi/PSecPkgContext_Sizes, sspi/SecPkgContext_Sizes"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
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
 - SecPkgContext_Sizes
product: Windows
targetos: Windows
req.typenames: SecPkgContext_Sizes, *PSecPkgContext_Sizes
req.redist: 
---

# _SecPkgContext_Sizes structure


## -description


The <b>SecPkgContext_Sizes</b> structure indicates the sizes of important structures used in the message support functions. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.


## -struct-fields




### -field cbMaxToken

Specifies the maximum size of the security token used in the authentication exchanges.


### -field cbMaxSignature

Specifies the maximum size of the signature created by the 
<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function. This member must be zero if <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> services are not requested or available.


### -field cbBlockSize

Specifies the preferred integral size of the messages. For example, eight indicates that messages should be of size zero mod eight for optimal performance. Messages other than this block size can be padded.


### -field cbSecurityTrailer

Size of the security trailer to be appended to messages. This member should be zero if the relevant services are not requested or available.


## -see-also




<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a>



<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>
 

 

