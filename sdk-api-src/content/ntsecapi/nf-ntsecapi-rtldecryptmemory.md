---
UID: NF:ntsecapi.RtlDecryptMemory
title: RtlDecryptMemory function
author: windows-sdk-content
description: Decrypts memory contents previously encrypted by the RtlEncryptMemory function.
old-location: security\rtldecryptmemory.htm
tech.root: seccrypto
ms.assetid: 8ecc5007-92ce-4e32-a093-dcb75ee8ba62
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: RTL_ENCRYPT_OPTION_CROSS_PROCESS, RTL_ENCRYPT_OPTION_SAME_LOGON, RtlDecryptMemory, RtlDecryptMemory function [Security], ntsecapi/RtlDecryptMemory, security.rtldecryptmemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows Server 2003 [desktop apps only]
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
 - RtlDecryptMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlDecryptMemory function


## -description


<p class="CCE_Message">[The <b>RtlDecryptMemory</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/1c7980ac-4e9e-43fd-b6d7-c0d0a69c8040">CryptUnprotectMemory</a> function.]

The <b>RtlDecryptMemory</b> function decrypts memory contents previously encrypted by the <a href="https://msdn.microsoft.com/b124a7fe-c62c-42f7-9d2b-cbf74d17186a">RtlEncryptMemory</a> function.
<div class="alert"><b>Note</b>  This function has no associated import library. This function is available as a resource named <b>SystemFunction041</b> in Advapi32.dll. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Advapi32.dll.</div><div> </div>

## -parameters




### -param Memory [in, out]

A pointer to the memory to encrypt. The size of the memory must be a multiple of the RTL_ENCRYPT_MEMORY_SIZE constant.


### -param MemorySize [in]

Number of bytes to which <i>Memory</i> points. The number of bytes must be a multiple of the RTL_ENCRYPT_MEMORY_SIZE constant.


### -param OptionFlags [in]

Value that specifies how the encryption works over process boundaries and impersonation. This parameter can be one of the following values. The values are mutually exclusive. You must specify the same flag when encrypting and decrypting the memory.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Encrypt and decrypt memory in the same process. An application running in a different process will not be able to decrypt the data.

</td>
</tr>
<tr>
<td width="40%"><a id="RTL_ENCRYPT_OPTION_CROSS_PROCESS"></a><a id="rtl_encrypt_option_cross_process"></a><dl>
<dt><b>RTL_ENCRYPT_OPTION_CROSS_PROCESS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data.

</td>
</tr>
<tr>
<td width="40%"><a id="RTL_ENCRYPT_OPTION_SAME_LOGON"></a><a id="rtl_encrypt_option_same_logon"></a><dl>
<dt><b>RTL_ENCRYPT_OPTION_SAME_LOGON</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Use the same logon credentials to encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data. However, the process must run as the same user that encrypted the data and in the same logon session.

</td>
</tr>
</table>
 


## -returns



If the function is successful, the return value is STATUS_SUCCESS.

If the function fails, the return value is an <b>NTSTATUS</b> code that indicates the error.



