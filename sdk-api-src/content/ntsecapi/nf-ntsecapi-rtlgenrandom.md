---
UID: NF:ntsecapi.RtlGenRandom
title: RtlGenRandom function (ntsecapi.h)
author: windows-sdk-content
description: Generates a pseudo-random number.
old-location: security\rtlgenrandom.htm
tech.root: SecCrypto
ms.assetid: 0b0d7019-49a1-40d0-912d-c773bce09a26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtlGenRandom, RtlGenRandom function [Security], ntsecapi/RtlGenRandom, security.rtlgenrandom
ms.topic: function
f1_keywords: 
 - "ntsecapi/RtlGenRandom"
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
req.lib: 
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
 - RtlGenRandom
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtlGenRandom function


## -description


<p class="CCE_Message">[The <b>RtlGenRandom</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom">CryptGenRandom</a> function.]

The <b>RtlGenRandom</b> function  generates a pseudo-random number.
<div class="alert"><b>Note</b>  This function has no associated import library. This function is available as a resource named <b>SystemFunction036</b> in Advapi32.dll. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Advapi32.dll.</div><div> </div>

## -parameters




### -param RandomBuffer [out]

A pointer to a buffer that receives the random number as binary data. The size of this buffer is specified by the <i>RandomBufferLength</i> parameter.


### -param RandomBufferLength [in]

The length, in bytes, of the <i>RandomBuffer</i> buffer.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



When you have finished using the random number, free the <i>RandomBuffer</i> buffer by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function.



