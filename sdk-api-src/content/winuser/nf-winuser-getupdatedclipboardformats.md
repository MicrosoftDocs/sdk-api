---
UID: NF:winuser.GetUpdatedClipboardFormats
title: GetUpdatedClipboardFormats function (winuser.h)
description: Retrieves the currently supported clipboard formats.
helpviewer_keywords: ["GetUpdatedClipboardFormats","GetUpdatedClipboardFormats function [Data Exchange]","_win32_GetUpdatedClipboardFormats","_win32_getupdatedclipboardformats_cpp","dataxchg.getupdatedclipboardformats","winui._win32_getupdatedclipboardformats","winuser/GetUpdatedClipboardFormats"]
old-location: dataxchg\getupdatedclipboardformats.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getupdatedclipboardformats.htm
ms.date: 12/05/2018
ms.keywords: GetUpdatedClipboardFormats, GetUpdatedClipboardFormats function [Data Exchange], _win32_GetUpdatedClipboardFormats, _win32_getupdatedclipboardformats_cpp, dataxchg.getupdatedclipboardformats, winui._win32_getupdatedclipboardformats, winuser/GetUpdatedClipboardFormats
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetUpdatedClipboardFormats
 - winuser/GetUpdatedClipboardFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetUpdatedClipboardFormats
---

# GetUpdatedClipboardFormats function


## -description

Retrieves the currently supported clipboard formats.

## -parameters

### -param lpuiFormats [out]

Type: <b>PUINT</b>

An array of clipboard formats. For a description of the standard clipboard formats, see <a href="/windows/desktop/dataxchg/standard-clipboard-formats">Standard Clipboard Formats</a>.

### -param cFormats [in]

Type: <b>UINT</b>

The number of entries in the array pointed to by <i>lpuiFormats</i>.

### -param pcFormatsOut [out]

Type: <b>PUINT</b>

The actual number of clipboard formats in the array pointed to by <i>lpuiFormats</i>.

## -returns

Type: <b>BOOL</b>

The function returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for additional details.