---
UID: NS:sspi._SecBufferDesc
title: "_SecBufferDesc"
author: windows-driver-content
description: The SecBufferDesc structure describes an array of SecBuffer structures to pass from a transport application to a security package.
old-location: security\secbufferdesc.htm
old-project: SecAuthN
ms.assetid: fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PSecBufferDesc, PSecBufferDesc, PSecBufferDesc structure pointer [Security], SecBufferDesc, SecBufferDesc structure [Security], _SecBufferDesc, _ssp_secbufferdesc, security.secbufferdesc, sspi/PSecBufferDesc, sspi/SecBufferDesc"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SecBufferDesc, *PSecBufferDesc
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecBufferDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _SecBufferDesc structure


## -description



			The <b>SecBufferDesc</b> structure describes an array of <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures to pass from a transport application to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.
		


## -struct-fields




### -field ulVersion

Specifies the version number of this structure. This member must be SECBUFFER_VERSION.


### -field cBuffers

Indicates the number of <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures in the <b>pBuffers</b> array.


### -field pBuffers

Pointer to an array of <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures.


### -field pBuffers.size_is

 


### -field pBuffers.size_is.cBuffers

 




## -see-also




<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>
 

 

