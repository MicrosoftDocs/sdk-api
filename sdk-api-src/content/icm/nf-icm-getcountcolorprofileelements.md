---
UID: NF:icm.GetCountColorProfileElements
title: GetCountColorProfileElements
description: Retrieves the number of tagged elements in a given color profile.
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
 - GetCountColorProfileElements
f1_keywords:
 - GetCountColorProfileElements
 - icm/GetCountColorProfileElements
dev_langs:
 - c++
---

## -description

Retrieves the number of tagged elements in a given color profile.

## -parameters

### -param hProfile

Specifies a handle to the profile in question.

### -param pnElementCount

Pointer to a variable in which to place the number of tagged elements in the profile.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
