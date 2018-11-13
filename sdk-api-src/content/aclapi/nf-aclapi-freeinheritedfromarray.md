---
UID: NF:aclapi.FreeInheritedFromArray
title: FreeInheritedFromArray function
author: windows-sdk-content
description: Frees memory allocated by the GetInheritanceSource function.
old-location: security\freeinheritedfromarray.htm
tech.root: SecAuthZ
ms.assetid: c9c58b9a-1b65-40e2-b518-30e247f9718e
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: FreeInheritedFromArray, FreeInheritedFromArray function [Security], _win32_freeinheritedfromarray, aclapi/FreeInheritedFromArray, security.freeinheritedfromarray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - FreeInheritedFromArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeInheritedFromArray function


## -description


The <b>FreeInheritedFromArray</b> function frees memory allocated by the 
<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a> function.


## -parameters




### -param pInheritArray [in]

A pointer to the array of <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structures returned by <a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>.


### -param AceCnt [in]

Number of entries in <i>pInheritArray</i>.


### -param pfnArray [in, optional]

Unused. Set to <b>NULL</b>.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>
 

 

