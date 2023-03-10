---
UID: NF:icm.GetColorProfileElement
title: GetColorProfileElement
description: Copies data from a specified tagged profile element of a specified color profile into a buffer.
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
 - GetColorProfileElement
f1_keywords:
 - GetColorProfileElement
 - icm/GetColorProfileElement
dev_langs:
 - c++
---

## -description

Copies data from a specified tagged profile element of a specified color profile into a buffer.

## -parameters

### -param hProfile

Specifies a handle to the International Color Consortium (ICC) color profile in question.

### -param tag

Identifies the tagged element from which to copy.

### -param dwOffset

Specifies the offset from the first byte of the tagged element data at which to begin copying.

### -param pcbElement

Pointer to a variable specifying the number of bytes to copy. On return, the variable contains the number of bytes actually copied.

### -param pElement

Pointer to a buffer into which the tagged element data is to be copied. The buffer must contain at least as many bytes as are specified by the variable pointed to by *pcbSize*. If the *pBuffer* pointer is set to **NULL**, the size of the entire tagged element data in bytes is returned in the memory location pointed to by *pcbSize,* and *dwOffset* is ignored. In this case, the function will return **FALSE**.

### -param pbReference

Points to a Boolean value that is set to **TRUE** if more than one tag in the color profile refers to the same data as the specified tag refers to, or **FALSE** if not.

## -returns

If this function succeeds, the return value is nonzero.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid International Color Consortium (ICC) profile.

If the *pBuffer* pointer is set to **NULL**, the size of the entire tagged element data in bytes is returned in the variable pointed to by *pcbSize,* and *dwOffset* is ignored.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with, and hard coded to, ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
