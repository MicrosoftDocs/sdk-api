---
UID: NE:mbnapi.MBN_CONTEXT_CONSTANTS
title: MBN_CONTEXT_CONSTANTS (mbnapi.h)
description: The MBN_CONTEXT_CONSTANTS enumerated type specifies the maximum string lengths supported by members of the MBN_CONTEXT structure.
helpviewer_keywords: ["MBN_ACCESSSTRING_LEN","MBN_CONTEXT_CONSTANTS","MBN_CONTEXT_CONSTANTS enumeration [Microsoft Broadband Networks]","MBN_CONTEXT_ID_APPEND","MBN_PASSWORD_LEN","MBN_USERNAME_LEN","mbn.mbn_context_constants","mbnapi/MBN_ACCESSSTRING_LEN","mbnapi/MBN_CONTEXT_CONSTANTS","mbnapi/MBN_CONTEXT_ID_APPEND","mbnapi/MBN_PASSWORD_LEN","mbnapi/MBN_USERNAME_LEN"]
old-location: mbn\mbn_context_constants.htm
tech.root: mbn
ms.assetid: 064ff090-eb45-4cfa-99bd-d92db8397fc3
ms.date: 12/05/2018
ms.keywords: MBN_ACCESSSTRING_LEN, MBN_CONTEXT_CONSTANTS, MBN_CONTEXT_CONSTANTS enumeration [Microsoft Broadband Networks], MBN_CONTEXT_ID_APPEND, MBN_PASSWORD_LEN, MBN_USERNAME_LEN, mbn.mbn_context_constants, mbnapi/MBN_ACCESSSTRING_LEN, mbnapi/MBN_CONTEXT_CONSTANTS, mbnapi/MBN_CONTEXT_ID_APPEND, mbnapi/MBN_PASSWORD_LEN, mbnapi/MBN_USERNAME_LEN
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_CONTEXT_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_CONTEXT_CONSTANTS
 - mbnapi/MBN_CONTEXT_CONSTANTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_CONTEXT_CONSTANTS
---

# MBN_CONTEXT_CONSTANTS enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_CONTEXT_CONSTANTS</b> enumerated type specifies the maximum string lengths supported by members of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> structure.

## -enum-fields

### -field MBN_ACCESSSTRING_LEN:100

Maximum string length of the <b>accessString</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> structure.

### -field MBN_USERNAME_LEN:255

Maximum string length of the <b>userName</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> structure.

### -field MBN_PASSWORD_LEN:255

Maximum string length of the <b>password</b> member of the <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> structure.

### -field MBN_CONTEXT_ID_APPEND:0xffffffff

 The device will find the appropriate index to store a context into.
