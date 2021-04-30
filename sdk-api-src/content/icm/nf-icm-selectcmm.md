---
UID: NF:icm.SelectCMM
title: SelectCMM
description: Allows you to select the preferred color management module (CMM) to use.
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
 - SelectCMM
f1_keywords:
 - SelectCMM
 - icm/SelectCMM
dev_langs:
 - c++
---

## -description

Allows you to select the preferred color management module (CMM) to use.

## -parameters

### -param dwCMMType

Specifies the signature of the desired CMM as registered with the International Color Consortium (ICC).

**Windows 2000 only:** Setting this parameter to **NULL** causes the WCS system to select the default CMM.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

For **SelectCMM** to succeed, the specified CMM must be registered with the system.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
