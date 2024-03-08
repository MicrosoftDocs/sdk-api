---
UID: NF:winternl.RtlConvertSidToUnicodeString
title: RtlConvertSidToUnicodeString function (winternl.h)
description: Converts a security identifier (SID) to its Unicode character representation.
helpviewer_keywords: ["RtlConvertSidToUnicodeString","RtlConvertSidToUnicodeString function [Security]","security.rtlconvertsidtounicodestring","winternl/RtlConvertSidToUnicodeString"]
old-location: security\rtlconvertsidtounicodestring.htm
tech.root: security
ms.assetid: 4b2584ad-6752-46d4-83fb-3de0b783e229
ms.date: 12/05/2018
ms.keywords: RtlConvertSidToUnicodeString, RtlConvertSidToUnicodeString function [Security], security.rtlconvertsidtounicodestring, winternl/RtlConvertSidToUnicodeString
req.header: winternl.h
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlConvertSidToUnicodeString
 - winternl/RtlConvertSidToUnicodeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlConvertSidToUnicodeString
---

# RtlConvertSidToUnicodeString function


## -description

<p class="CCE_Message">[The <b>RtlConvertSidToUnicodeString</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida">ConvertSidToStringSid</a> function.]

The <b>RtlConvertSidToUnicodeString</b> function converts a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to its Unicode character representation. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

## -parameters

### -param UnicodeString [out]

A pointer to the Unicode character representation of the security identifier.

### -param Sid [in]

A pointer to the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the security identifier.

### -param AllocateDestinationString [in]

If <b>TRUE</b>, then  <i>UnicodeString</i> is allocated on behalf of the caller, and it is the caller's responsibility to free the allocated memory by calling the <b>RtlFreeUnicodeString</b> function. If <b>FALSE</b>, the caller is responsible for allocating and freeing  <i>UnicodeString</i>.

## -returns

The return value is an  NTSTATUS code. A value of STATUS_SUCCESS (0x00000000L) is returned if the function succeeds.