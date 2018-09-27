---
UID: NE:mbnapi.MBN_CONTEXT_CONSTANTS
title: MBN_CONTEXT_CONSTANTS
author: windows-sdk-content
description: The MBN_CONTEXT_CONSTANTS enumerated type specifies the maximum string lengths supported by members of the MBN_CONTEXT structure.
old-location: mbn\mbn_context_constants.htm
tech.root: mbn
ms.assetid: 064ff090-eb45-4cfa-99bd-d92db8397fc3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MBN_ACCESSSTRING_LEN, MBN_CONTEXT_CONSTANTS, MBN_CONTEXT_CONSTANTS enumeration [Microsoft Broadband Networks], MBN_CONTEXT_ID_APPEND, MBN_PASSWORD_LEN, MBN_USERNAME_LEN, mbn.mbn_context_constants, mbnapi/MBN_ACCESSSTRING_LEN, mbnapi/MBN_CONTEXT_CONSTANTS, mbnapi/MBN_CONTEXT_ID_APPEND, mbnapi/MBN_PASSWORD_LEN, mbnapi/MBN_USERNAME_LEN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_CONTEXT_CONSTANTS
product: Windows
targetos: Windows
req.typenames: MBN_CONTEXT_CONSTANTS
req.redist: 
---

# MBN_CONTEXT_CONSTANTS enumeration


## -description


The <b>MBN_CONTEXT_CONSTANTS</b> enumerated type specifies the maximum string lengths supported by members of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


## -enum-fields




### -field MBN_ACCESSSTRING_LEN

Maximum string length of the <b>accessString</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_USERNAME_LEN

Maximum string length of the <b>userName</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_PASSWORD_LEN

Maximum string length of the <b>password</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_CONTEXT_ID_APPEND

 The device will find the appropriate index to store a context into.

