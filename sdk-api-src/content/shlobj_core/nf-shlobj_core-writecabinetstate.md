---
UID: NF:shlobj_core.WriteCabinetState
title: WriteCabinetState function (shlobj_core.h)
description: WriteCabinetState may be altered or unavailable.
helpviewer_keywords: ["WriteCabinetState","WriteCabinetState function [Windows Shell]","_win32_WriteCabinetState","shell.WriteCabinetState","shlobj_core/WriteCabinetState"]
old-location: shell\WriteCabinetState.htm
tech.root: shell
ms.assetid: cbd08812-eedc-4ba7-827e-1e5d1e3e6368
ms.date: 12/05/2018
ms.keywords: WriteCabinetState, WriteCabinetState function [Windows Shell], _win32_WriteCabinetState, shell.WriteCabinetState, shlobj_core/WriteCabinetState
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
 - WriteCabinetState
 - shlobj_core/WriteCabinetState
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
 - WriteCabinetState
---

# WriteCabinetState function


## -description

<p class="CCE_Message">[<b>WriteCabinetState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Writes the information contained in a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a> structure into the registry.

## -parameters

### -param pcs [in]

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a>*</b>

A pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-cabinetstate">CABINETSTATE</a> structure that holds the values to be set.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.