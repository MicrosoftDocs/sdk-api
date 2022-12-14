---
UID: NF:icm.GetCMMInfo
title: GetCMMInfo
description: Retrieves various information about the color management module (CMM) that created the specified color transform.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - mscms.dll
api_name:
 - GetCMMInfo
f1_keywords:
 - GetCMMInfo
 - icm/GetCMMInfo
dev_langs:
 - c++
---

## -description

Retrieves various information about the color management module (CMM) that created the specified color transform.

## -parameters

### -param hColorTransform

Identifies the transform for which to find CMM information.

### -param unnamedParam2

Specifies the information to be retrieved. This parameter can take one of the following constant values.

| Value | Meaning |
|-|-|
| <span id="CMM_WIN_VERSION"></span><span id="cmm_win_version"></span><dl> <dt>**CMM\_WIN\_VERSION**</dt> </dl> | Retrieves the version of Windows targeted by the color management module (CMM).<br/> |
| <span id="CMM_DLL_VERSION"></span><span id="cmm_dll_version"></span><dl> <dt>**CMM\_DLL\_VERSION**</dt> </dl> | Retrieves the version number of the CMM.<br/> |
| <span id="CMM_IDENT"></span><span id="cmm_ident"></span><dl> <dt>**CMM\_IDENT**</dt> </dl> | Retrieves the CMM signature registered with the International Color Consortium (ICC).<br/> |

## -returns

If this function succeeds, the return value is the information specified in *dwInfo.*

If this function fails, the return value is zero.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
