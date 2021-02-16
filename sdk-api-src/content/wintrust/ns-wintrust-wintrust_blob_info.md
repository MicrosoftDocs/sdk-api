---
UID: NS:wintrust.WINTRUST_BLOB_INFO_
title: WINTRUST_BLOB_INFO (wintrust.h)
description: Used when calling WinVerifyTrust to verify a memory BLOB.
helpviewer_keywords: ["*PWINTRUST_BLOB_INFO","PWINTRUST_BLOB_INFO","PWINTRUST_BLOB_INFO structure pointer [Security]","WINTRUST_BLOB_INFO","WINTRUST_BLOB_INFO structure [Security]","_win32_wintrust_blob_info","security.wintrust_blob_info","wintrust/PWINTRUST_BLOB_INFO","wintrust/WINTRUST_BLOB_INFO"]
old-location: security\wintrust_blob_info.htm
tech.root: security
ms.assetid: 8b13d355-4d24-4d8e-aae3-db16467999be
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_BLOB_INFO, PWINTRUST_BLOB_INFO, PWINTRUST_BLOB_INFO structure pointer [Security], WINTRUST_BLOB_INFO, WINTRUST_BLOB_INFO structure [Security], _win32_wintrust_blob_info, security.wintrust_blob_info, wintrust/PWINTRUST_BLOB_INFO, wintrust/WINTRUST_BLOB_INFO'
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
targetos: Windows
req.typenames: WINTRUST_BLOB_INFO, *PWINTRUST_BLOB_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_BLOB_INFO_
 - wintrust/WINTRUST_BLOB_INFO_
 - PWINTRUST_BLOB_INFO
 - wintrust/PWINTRUST_BLOB_INFO
 - WINTRUST_BLOB_INFO
 - wintrust/WINTRUST_BLOB_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_BLOB_INFO
---

# WINTRUST_BLOB_INFO structure


## -description

<p class="CCE_Message">[The  <b>WINTRUST_BLOB_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_BLOB_INFO</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to verify a memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.<div class="alert"><b>Note</b>  This structure is not currently supported for the following Inbox file formats. There may be other formats besides these that are not supported. <ul>
<li>Portable executable (such as .exe, .dll, .ocx)</li>
<li>Cab files (.cab)</li>
<li>Catalog files (.cat)</li>
</ul>This structure is only supported by files formats with <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) providers that support this structure.</div>
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