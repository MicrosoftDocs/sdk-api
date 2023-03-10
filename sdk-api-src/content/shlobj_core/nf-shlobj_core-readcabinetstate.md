---
UID: NF:shlobj_core.ReadCabinetState
title: ReadCabinetState function (shlobj_core.h)
description: ReadCabinetState may be altered or unavailable.
helpviewer_keywords: ["ReadCabinetState","ReadCabinetState function [Windows Shell]","_win32_ReadCabinetState","shell.ReadCabinetState","shlobj_core/ReadCabinetState"]
old-location: shell\ReadCabinetState.htm
tech.root: shell
ms.assetid: 0f0c6a10-588f-4c79-b73b-cf0bf9336ffc
ms.date: 12/05/2018
ms.keywords: ReadCabinetState, ReadCabinetState function [Windows Shell], _win32_ReadCabinetState, shell.ReadCabinetState, shlobj_core/ReadCabinetState
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReadCabinetState
 - shlobj_core/ReadCabinetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - ReadCabinetState
---

# ReadCabinetState function


## -description

<p class="CCE_Message">[<b>ReadCabinetState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Fills a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a> structure with information from the registry.

## -parameters

### -param pcs [out]

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a>*</b>

When this function returns, contains a pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a> structure that contains either information pulled from the registry or default information.

### -param cLength [in]

Type: <b>int</b>

The size of the structure pointed to by <i>pcs</i>, in bytes.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the returned structure contains information from the registry. Returns <b>FALSE</b> if the structure contains default information.