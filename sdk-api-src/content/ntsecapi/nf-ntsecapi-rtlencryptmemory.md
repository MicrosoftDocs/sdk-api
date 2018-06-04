---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RtlEncryptMemory function


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/8ecc5007-92ce-4e32-a093-dcb75ee8ba62">RtlDecryptMemory</a> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/6b372552-87d4-4047-afa5-0d1113348289">CryptProtectMemory</a> function.]

The <b>RtlEncryptMemory</b> function encrypts memory contents.   The encrypted contents can be decrypted by a subsequent call to the <a href="https://msdn.microsoft.com/8ecc5007-92ce-4e32-a093-dcb75ee8ba62">RtlDecryptMemory</a> function.
<div class="alert"><b>Note</b>  This function has no associated import library. This function is available as a resource named <b>SystemFunction040</b> in Advapi32.dll. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Advapi32.dll.</div><div> </div>

## -parameters




### -param Memory [in, out]

A pointer to the memory to encrypt. The size of the memory must be a multiple of the RTL_ENCRYPT_MEMORY_SIZE constant.


### -param MemorySize

TBD


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
 


#### - MemoryLength [in]

Number of bytes to which <i>Memory</i> points. The number of bytes must be a multiple of the RTL_ENCRYPT_MEMORY_SIZE constant.


## -returns



If the function is successful, the return value is STATUS_SUCCESS.

If the function fails, the return value is an <b>NTSTATUS</b> code that indicates the error.



