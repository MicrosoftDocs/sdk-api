---
UID: NF:wincrypt.GetEncSChannel
title: GetEncSChannel function
author: windows-sdk-content
description: This function is unavailable.
old-location: security\getencschannel.htm
tech.root: seccrypto
ms.assetid: 4879895e-8bf4-4464-a344-04e4b361c5c7
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetEncSChannel, GetEncSChannel function [Security], security.getencschannel, wincrypt/GetEncSChannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
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
req.lib: 
req.dll: Instrsa5.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Instrsa5.dll
api_name:
 - GetEncSChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetEncSChannel function


## -description


<p class="CCE_Message">[The GetEncSChannel function is no longer available for use as of Windows Server 2003 and Windows XP.]
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Instrsa5.dll.</div><div> </div>

## -parameters




### -param pData [out]

A pointer to a pointer to bytes that receive the encrypted Schannel contents. When you have finished using the Schannel contents, free <i>pData</i> by calling the <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a> function.


### -param dwDecSize [out]

Number of bytes allocated for <i>pData</i>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>



