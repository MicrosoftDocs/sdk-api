---
UID: NS:sspi._SEC_WINNT_CREDUI_CONTEXT_VECTOR
title: "_SEC_WINNT_CREDUI_CONTEXT_VECTOR"
author: windows-driver-content
description: Specifies the offset and size of the credential context data in a SEC_WINNT_CREDUI_CONTEXT structure.
old-location: security\sec_winnt_credui_context_vector.htm
old-project: SecAuthN
ms.assetid: 11a82e82-f5c5-4549-8e5f-9d479e9c8249
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PSEC_WINNT_CREDUI_CONTEXT_VECTOR, PSEC_WINNT_CREDUI_CONTEXT_VECTOR, PSEC_WINNT_CREDUI_CONTEXT_VECTOR structure pointer [Security], SEC_WINNT_CREDUI_CONTEXT_VECTOR, SEC_WINNT_CREDUI_CONTEXT_VECTOR structure [Security], _SEC_WINNT_CREDUI_CONTEXT_VECTOR, security.sec_winnt_credui_context_vector, sspi/PSEC_WINNT_CREDUI_CONTEXT_VECTOR, sspi/SEC_WINNT_CREDUI_CONTEXT_VECTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SEC_WINNT_CREDUI_CONTEXT_VECTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _SEC_WINNT_CREDUI_CONTEXT_VECTOR structure


## -description


Specifies the offset and size of the credential context data in a <a href="https://msdn.microsoft.com/ac9410eb-ec1b-494c-8e8b-6d161ff2b41c">SEC_WINNT_CREDUI_CONTEXT</a> structure.


## -struct-fields




### -field CredUIContextArrayOffset

The number of bytes from the  beginning of the structure to the context data.


### -field CredUIContextCount

The size, in bytes, of the context data.

