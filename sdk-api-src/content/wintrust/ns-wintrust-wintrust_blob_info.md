---
UID: NS:wintrust.WINTRUST_BLOB_INFO_
title: WINTRUST_BLOB_INFO (wintrust.h)
author: windows-sdk-content
description: Used when calling WinVerifyTrust to verify a memory BLOB.
old-location: security\wintrust_blob_info.htm
tech.root: SecCrypto
ms.assetid: 8b13d355-4d24-4d8e-aae3-db16467999be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWINTRUST_BLOB_INFO, PWINTRUST_BLOB_INFO, PWINTRUST_BLOB_INFO structure pointer [Security], WINTRUST_BLOB_INFO, WINTRUST_BLOB_INFO structure [Security], _win32_wintrust_blob_info, security.wintrust_blob_info, wintrust/PWINTRUST_BLOB_INFO, wintrust/WINTRUST_BLOB_INFO"
ms.topic: struct
req.header: wintrust.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_BLOB_INFO
product: Windows
targetos: Windows
req.typenames: WINTRUST_BLOB_INFO, *PWINTRUST_BLOB_INFO
req.redist: 
---

# WINTRUST_BLOB_INFO structure


## -description


<p class="CCE_Message">[The  <b>WINTRUST_BLOB_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_BLOB_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a memory <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.<div class="alert"><b>Note</b>  This structure is not currently supported for the following Inbox file formats. There may be other formats besides these that are not supported. <ul>
<li>Portable executable (such as .exe, .dll, .ocx)</li>
<li>Cab files (.cab)</li>
<li>Catalog files (.cat)</li>
</ul>This structure is only supported by files formats with <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) providers that support this structure.</div>
<div> </div>



## -struct-fields




### -field cbStruct

The number of bytes in this structure.


### -field gSubject

The <b>GUID</b> of the SIP to load.


### -field pcwszDisplayName

A string that contains the name of the memory object pointed to by <b>pbMem</b>.


### -field cbMemObject

The length, in bytes, of the memory BLOB to be verified.


### -field pbMemObject

A pointer to a memory BLOB to be verified.


### -field cbMemSignedMsg

This member is reserved. Do not use it.


### -field pbMemSignedMsg

This member is reserved. Do not use it.

