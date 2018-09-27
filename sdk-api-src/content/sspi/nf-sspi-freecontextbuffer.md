---
UID: NF:sspi.FreeContextBuffer
title: FreeContextBuffer function
author: windows-sdk-content
description: Enables callers of security package functions to free memory buffers allocated by the security package.
old-location: security\freecontextbuffer.htm
tech.root: secauthn
ms.assetid: 3c3d27bb-4f9a-4979-b679-1e10fa1ff221
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FreeContextBuffer, FreeContextBuffer function [Security], _ssp_freecontextbuffer, security.freecontextbuffer, sspi/FreeContextBuffer
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
req.unicode-ansi: 
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
api_name:
 - FreeContextBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeContextBuffer function


## -description


The <b>FreeContextBuffer</b> function enables callers of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> functions to free memory buffers allocated by the security package.


## -parameters




### -param pvContextBuffer [in]

A pointer to memory to be freed.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code.




## -remarks



Memory buffers are typically allocated by the  <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> and <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> functions.

The <b>FreeContextBuffer</b> function can free any memory allocated by a security package.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 

