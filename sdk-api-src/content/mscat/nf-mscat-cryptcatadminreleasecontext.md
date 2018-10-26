---
UID: NF:mscat.CryptCATAdminReleaseContext
title: CryptCATAdminReleaseContext function
author: windows-sdk-content
description: Releases the handle previously assigned by the CryptCATAdminAcquireContext function.
old-location: security\cryptcatadminreleasecontext.htm
tech.root: seccrypto
ms.assetid: dff253dc-c444-46be-a383-41340d634cce
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CryptCATAdminReleaseContext, CryptCATAdminReleaseContext function [Security], mscat/CryptCATAdminReleaseContext, security.cryptcatadminreleasecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mscat.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminReleaseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATAdminReleaseContext function


## -description


<p class="CCE_Message">[The  <b>CryptCATAdminReleaseContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminReleaseContext</b> function releases the handle previously assigned by the <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Catalog administrator context handle previously  assigned by a call to the <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param dwFlags [in]

Not used; set to  zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a>
 

 

