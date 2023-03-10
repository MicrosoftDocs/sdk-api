---
UID: NS:shlobj_core._NRESARRAY
title: NRESARRAY (shlobj_core.h)
description: Defines the CF_NETRESOURCE clipboard format.
helpviewer_keywords: ["*LPNRESARRAY","LPNRESARRAY","LPNRESARRAY structure pointer [Windows Shell]","NRESARRAY","NRESARRAY structure [Windows Shell]","_NRESARRAY","_win32_NRESARRAY","shell.NRESARRAY","shlobj_core/LPNRESARRAY","shlobj_core/NRESARRAY"]
old-location: shell\NRESARRAY.htm
tech.root: shell
ms.assetid: 261338c2-8fb4-4d10-8392-f9f6254a30ed
ms.date: 12/05/2018
ms.keywords: '*LPNRESARRAY, LPNRESARRAY, LPNRESARRAY structure pointer [Windows Shell], NRESARRAY, NRESARRAY structure [Windows Shell], _NRESARRAY, _win32_NRESARRAY, shell.NRESARRAY, shlobj_core/LPNRESARRAY, shlobj_core/NRESARRAY'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: NRESARRAY, *LPNRESARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NRESARRAY
 - shlobj_core/_NRESARRAY
 - LPNRESARRAY
 - shlobj_core/LPNRESARRAY
 - NRESARRAY
 - shlobj_core/NRESARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - NRESARRAY
---

# NRESARRAY structure


## -description

Defines the CF_NETRESOURCE clipboard format.

## -struct-fields

### -field cItems

Type: <b>UINT</b>

The number of elements in the <b>nr</b> array.

### -field nr

Type: <b><a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>[1]</b>

The array of <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a> structures that contain information about network resources. The string members (<b>LPSTR</b> types) in the structure contain offsets instead of addresses.