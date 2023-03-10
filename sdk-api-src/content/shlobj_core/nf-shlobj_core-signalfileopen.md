---
UID: NF:shlobj_core.SignalFileOpen
title: SignalFileOpen function (shlobj_core.h)
description: SignalFileOpen may be altered or unavailable.
helpviewer_keywords: ["SignalFileOpen","SignalFileOpen function [Windows Shell]","_win32_SignalFileOpen","shell.SignalFileOpen","shlobj_core/SignalFileOpen"]
old-location: shell\SignalFileOpen.htm
tech.root: shell
ms.assetid: b46bb06f-a183-4a39-89bd-457fa4fe728f
ms.date: 12/05/2018
ms.keywords: SignalFileOpen, SignalFileOpen function [Windows Shell], _win32_SignalFileOpen, shell.SignalFileOpen, shlobj_core/SignalFileOpen
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
 - SignalFileOpen
 - shlobj_core/SignalFileOpen
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
 - SignalFileOpen
---

# SignalFileOpen function


## -description

<p class="CCE_Message">[<b>SignalFileOpen</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sends a notification to the Shell that the specified file has been opened.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that specifies the file.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise <b>FALSE</b>.

