---
UID: NS:shellapi._SHSTOCKICONINFO
title: SHSTOCKICONINFO (shellapi.h)
description: Receives information used to retrieve a stock Shell icon. This structure is used in a call SHGetStockIconInfo.
helpviewer_keywords: ["SHSTOCKICONINFO","SHSTOCKICONINFO structure [Windows Shell]","_SHSTOCKICONINFO","_SHSTOCKICONINFO structure [Windows Shell]","_shell_SHSTOCKICONINFO","shell.SHSTOCKICONINFO","shellapi/SHSTOCKICONINFO"]
old-location: shell\SHSTOCKICONINFO.htm
tech.root: shell
ms.assetid: 4d32826a-bb40-4805-9826-801c142b8d28
ms.date: 12/05/2018
ms.keywords: SHSTOCKICONINFO, SHSTOCKICONINFO structure [Windows Shell], _SHSTOCKICONINFO, _SHSTOCKICONINFO structure [Windows Shell], _shell_SHSTOCKICONINFO, shell.SHSTOCKICONINFO, shellapi/SHSTOCKICONINFO
req.header: shellapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHSTOCKICONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHSTOCKICONINFO
 - shellapi/_SHSTOCKICONINFO
 - SHSTOCKICONINFO
 - shellapi/SHSTOCKICONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - _SHSTOCKICONINFO
---

# SHSTOCKICONINFO structure


## -description

Receives information used to retrieve a stock Shell icon. This structure is used in a call <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a>.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.

### -field hIcon

Type: <b>HICON</b>

When <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a> is called with the SHGSI_ICON flag, this member receives a handle to the icon.

### -field iSysImageIndex

Type: <b>int</b>

When <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a> is called with the SHGSI_SYSICONINDEX flag, this member receives the index of the image in the system icon cache.

### -field iIcon

Type: <b>int</b>

When <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the index of the icon in the resource whose path is received in <b>szPath</b>.

### -field szPath

Type: <b>WCHAR[MAX_PATH]</b>

When <a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a> is called with the SHGSI_ICONLOCATION flag, this member receives the path of the resource that contains the icon. The index of the icon within the resource is received in <b>iIcon</b>.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-shgetstockiconinfo">SHGetStockIconInfo</a>