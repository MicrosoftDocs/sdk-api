---
UID: NF:ntsecapi.RtlGenRandom
title: RtlGenRandom function
author: windows-driver-content
description: Generates a pseudo-random number.
old-location: security\rtlgenrandom.htm
old-project: SecCrypto
ms.assetid: 0b0d7019-49a1-40d0-912d-c773bce09a26
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: RtlGenRandom, RtlGenRandom function [Security], ntsecapi/RtlGenRandom, security.rtlgenrandom
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	RtlGenRandom
product: Windows
targetos: Windows
req.lib: 
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RtlGenRandom function


## -description


<p class="CCE_Message">[The <b>RtlGenRandom</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> function.]

The <b>RtlGenRandom</b> function  generates a pseudo-random number.
<div class="alert"><b>Note</b>  This function has no associated import library. This function is available as a resource named <b>SystemFunction036</b> in Advapi32.dll. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Advapi32.dll.</div><div> </div>

## -parameters




### -param RandomBuffer [out]

A pointer to a buffer that receives the random number as binary data. The size of this buffer is specified by the <i>RandomBufferLength</i> parameter.


### -param RandomBufferLength [in]

The length, in bytes, of the <i>RandomBuffer</i> buffer.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



When you have finished using the random number, free the <i>RandomBuffer</i> buffer by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function.



