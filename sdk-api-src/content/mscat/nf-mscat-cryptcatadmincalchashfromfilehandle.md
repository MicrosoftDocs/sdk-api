---
UID: NF:mscat.CryptCATAdminCalcHashFromFileHandle
title: CryptCATAdminCalcHashFromFileHandle function
author: windows-driver-content
description: Calculates the hash for a file.
old-location: security\cryptcatadmincalchashfromfilehandle.htm
old-project: SecCrypto
ms.assetid: 4dc5688f-4b7a-4baf-9671-868cac7f1896
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CryptCATAdminCalcHashFromFileHandle, CryptCATAdminCalcHashFromFileHandle function [Security], mscat/CryptCATAdminCalcHashFromFileHandle, security.cryptcatadmincalchashfromfilehandle
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
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wintrust.dll
api_name:
-	CryptCATAdminCalcHashFromFileHandle
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATAdminCalcHashFromFileHandle function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminCalcHashFromFileHandle</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminCalcHashFromFileHandle</b> function calculates the hash for a file. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


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



