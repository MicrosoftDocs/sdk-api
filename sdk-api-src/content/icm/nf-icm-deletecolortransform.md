---
UID: NF:icm.DeleteColorTransform
title: DeleteColorTransform
description: Deletes a given color transform.
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
 - DeleteColorTransform
f1_keywords:
 - DeleteColorTransform
 - icm/DeleteColorTransform
dev_langs:
 - c++
---

## -description

Deletes a given color transform.

## -parameters

### -param hxform

Identifies the color transform to delete.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [COLOR structure](/windows/win32/api/icm/ns-icm-color)
* [CreateMultiProfileTransform](/windows/win32/api/icm/nf-icm-createmultiprofiletransform)
