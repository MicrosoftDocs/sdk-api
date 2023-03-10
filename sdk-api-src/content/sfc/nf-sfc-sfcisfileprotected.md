---
UID: NF:sfc.SfcIsFileProtected
title: SfcIsFileProtected function (sfc.h)
description: Determines whether the specified file is protected.
helpviewer_keywords: ["SfcIsFileProtected","SfcIsFileProtected function [Setup API]","_win32_sfcisfileprotected","setup.sfcisfileprotected","sfc/SfcIsFileProtected"]
old-location: setup\sfcisfileprotected.htm
tech.root: setup
ms.assetid: 6882f7ef-0265-4db5-afa5-54df35b9dba1
ms.date: 12/05/2018
ms.keywords: SfcIsFileProtected, SfcIsFileProtected function [Setup API], _win32_sfcisfileprotected, setup.sfcisfileprotected, sfc/SfcIsFileProtected
req.header: sfc.h
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
req.lib: Sfc.lib
req.dll: Sfc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SfcIsFileProtected
 - sfc/SfcIsFileProtected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sfc.dll
 - Ext-MS-Win-Wrp-Sfc-L1-1-0.dll
 - sfc_os.dll
api_name:
 - SfcIsFileProtected
---

# SfcIsFileProtected function


## -description

Determines whether the specified file is protected. Applications should avoid replacing protected system files.

## -parameters

### -param RpcHandle [in]

This parameter must be <b>NULL</b>.

### -param ProtFileName [in]

The name of the file.

## -returns

If the file is protected, the return value is a nonzero value.

If the file is not protected, the return value is zero.

## -see-also

<a href="/windows/desktop/api/sfc/nf-sfc-sfciskeyprotected">SfcIsKeyProtected</a>