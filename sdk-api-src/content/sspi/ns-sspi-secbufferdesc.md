---
UID: NS:sspi._SecBufferDesc
title: SecBufferDesc (sspi.h)
author: windows-sdk-content
description: The SecBufferDesc structure describes an array of SecBuffer structures to pass from a transport application to a security package.
old-location: security\secbufferdesc.htm
tech.root: SecAuthN
ms.assetid: fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSecBufferDesc, PSecBufferDesc, PSecBufferDesc structure pointer [Security], SecBufferDesc, SecBufferDesc structure [Security], _ssp_secbufferdesc, security.secbufferdesc, sspi/PSecBufferDesc, sspi/SecBufferDesc"
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
 - SecBufferDesc
product: Windows
targetos: Windows
req.typenames: SecBufferDesc, *PSecBufferDesc
req.redist: 
ms.custom: 19H1
---

# SecBufferDesc structure


## -description


The <b>SecBufferDesc</b> structure describes an array of <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_secbuffer">SecBuffer</a> structures to pass from a transport application to a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a>.
		


## -struct-fields




### -field ulVersion

Specifies the version number of this structure. This member must be SECBUFFER_VERSION.


### -field cBuffers

Indicates the number of <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_secbuffer">SecBuffer</a> structures in the <b>pBuffers</b> array.


### -field pBuffers

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_secbuffer">SecBuffer</a> structures.


### -field pBuffers.size_is

 


### -field pBuffers.size_is.cBuffers

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-_secbuffer">SecBuffer</a>
 

 

