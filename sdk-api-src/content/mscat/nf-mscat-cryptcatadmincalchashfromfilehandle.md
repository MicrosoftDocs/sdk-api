---
UID: NF:mscat.CryptCATAdminCalcHashFromFileHandle
title: CryptCATAdminCalcHashFromFileHandle function (mscat.h)
description: Calculates the hash for a file.
helpviewer_keywords: ["CryptCATAdminCalcHashFromFileHandle","CryptCATAdminCalcHashFromFileHandle function [Security]","mscat/CryptCATAdminCalcHashFromFileHandle","security.cryptcatadmincalchashfromfilehandle"]
old-location: security\cryptcatadmincalchashfromfilehandle.htm
tech.root: security
ms.assetid: 4dc5688f-4b7a-4baf-9671-868cac7f1896
ms.date: 12/05/2018
ms.keywords: CryptCATAdminCalcHashFromFileHandle, CryptCATAdminCalcHashFromFileHandle function [Security], mscat/CryptCATAdminCalcHashFromFileHandle, security.cryptcatadmincalchashfromfilehandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATAdminCalcHashFromFileHandle
 - mscat/CryptCATAdminCalcHashFromFileHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
 - mscat32.dll
api_name:
 - CryptCATAdminCalcHashFromFileHandle
---

# CryptCATAdminCalcHashFromFileHandle function


## -description

<p class="CCE_Message">[The <b>CryptCATAdminCalcHashFromFileHandle</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminCalcHashFromFileHandle</b> function calculates the hash for a file. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hFile [in]

A handle to the file whose hash is being calculated. This parameter cannot be <b>NULL</b> and must be a valid file handle.

### -param pcbHash [in, out]

A pointer to a <b>DWORD</b> variable that contains the number of bytes in <i>pbHash</i>. Upon input, set <i>pcbHash</i>  to the number of bytes allocated for <i>pbHash</i>. Upon return, <i>pcbHash</i> contains the number of returned bytes in  <i>pbHash</i>. If <i>pbHash</i> is passed as <b>NULL</b>, then <i>pcbHash</i> contains the number of bytes to allocate for  <i>pbHash</i>.

### -param pbHash [in]

A pointer to a <b>BYTE</b> buffer that receives the hash. If this parameter is passed in as <b>NULL</b>, then <i>pcbHash</i> contains the number of bytes to allocate for  <i>pbHash</i>, and a subsequent call can be made to retrieve the hash.

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If <b>FALSE</b> is returned, call the <b>GetLastError</b> function to determine the reason for failure. If not enough memory has been allocated for <i>pbHash</i>, the <b>CryptCATAdminCalcHashFromFileHandle</b> function will set the last error to ERROR_INSUFFICIENT_BUFFER.