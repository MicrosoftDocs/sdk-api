---
UID: NF:shellapi.SHGetImageList
title: SHGetImageList function (shellapi.h)
description: Retrieves an image list.
helpviewer_keywords: ["SHGetImageList","SHGetImageList function [Windows Shell]","SHIL_EXTRALARGE","SHIL_JUMBO","SHIL_LARGE","SHIL_LAST","SHIL_SMALL","SHIL_SYSSMALL","_shell_SHGetImageList","shell.SHGetImageList","shellapi/SHGetImageList"]
old-location: shell\SHGetImageList.htm
tech.root: shell
ms.assetid: 6ae80c1f-f2b7-4da9-b588-30391c8aef0e
ms.date: 12/05/2018
ms.keywords: SHGetImageList, SHGetImageList function [Windows Shell], SHIL_EXTRALARGE, SHIL_JUMBO, SHIL_LARGE, SHIL_LAST, SHIL_SMALL, SHIL_SYSSMALL, _shell_SHGetImageList, shell.SHGetImageList, shellapi/SHGetImageList
req.header: shellapi.h
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetImageList
 - shellapi/SHGetImageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
api_name:
 - SHGetImageList
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHGetImageList function


## -description

Retrieves an image list.

## -parameters

### -param iImageList [in]

Type: <b>int</b>

The image type contained in the list. One of the following values:

| Value | Description |
|---|---|
| **SHIL_LARGE** (0x0) | 32x32 pixels at 96 DPI; scales with DPI via **SM_CXICON** / **SM_CYICON**. |
| **SHIL_SMALL** (0x1) | 16x16 pixels at 96 DPI; scales with DPI via **SM_CXSMICON** / **SM_CYSMICON**. |
| **SHIL_EXTRALARGE** (0x2) | 48x48 pixels at 96 DPI; scales with DPI (48 logical pixels). |
| **SHIL_SYSSMALL** (0x3) | Tracks the caption button size (**SM_CXSMSIZE** / **SM_CYSMSIZE**). Typically matches **SHIL_SMALL** but may differ when the user customizes window border and caption size in Display Settings. |
| **SHIL_JUMBO** (0x4) | Windows Vista and later. Fixed at 256x256 physical pixels regardless of DPI. |
| **SHIL_LAST** | The largest valid flag value, for validation purposes. |

### -param riid [in]

Type: <b>REFIID</b>

Reference to the image list interface identifier, normally IID_IImageList.

### -param ppvObj [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">IImageList</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/commoncontrols/nn-commoncontrols-iimagelist">IImageList</a> pointer type, such as that returned in the <i>ppv</i> parameter, can be cast as an <b>HIMAGELIST</b> as needed; for example, for use in a list view. Conversely, an <b>HIMAGELIST</b> can be cast as a pointer to an <b>IImageList</b>.

As of Windows Vista, <b>SHIL_SMALL</b>, <b>SHIL_LARGE</b>, and <b>SHIL_EXTRALARGE</b> scale with dots per inch (dpi) if the process is marked as dpi-aware. To set these types to be dpi-aware, call <a href="/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a>. <b>SHIL_JUMBO</b> is fixed at 256 pixels regardless of the dpi-aware setting.

## -see-also

<a href="/windows/desktop/shell/fileiconinit">FileIconInit</a>
