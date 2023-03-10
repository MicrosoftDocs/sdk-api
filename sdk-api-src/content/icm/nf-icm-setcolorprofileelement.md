---
UID: NF:icm.SetColorProfileElement
title: SetColorProfileElement
description: Sets the element data for a tagged profile element in an ICC color profile.
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
 - SetColorProfileElement
f1_keywords:
 - SetColorProfileElement
 - icm/SetColorProfileElement
dev_langs:
 - c++
---

## -description

Sets the element data for a tagged profile element in an ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC profile in question.

### -param tag

Identifies the tagged element.

### -param dwOffset

Specifies the offset from the first byte of the tagged element data at which to start writing.

### -param pcbElement

Pointer to a variable containing the number of bytes of data to write. On return, it contains the number of bytes actually written.

### -param pElement

Pointer to a buffer containing the data to write to the tagged element in the color profile.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

If the color profile is not opened for read/write permission, this function fails.

If *dwOffset* exceeds the size set for the specified tagged element, this function fails.

If *dwOffset* + *\*pcbSize* is greater than the size of the specified element, this function only writes as many bytes as will fit within the current size of the element.

Any existing data in the specified portion of the tagged element is overwritten when this function succeeds.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
