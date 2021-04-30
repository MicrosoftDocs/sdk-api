---
UID: NF:icm.SetColorProfileElementSize
title: SetColorProfileElementSize
description: Sets the size of a tagged element in an ICC color profile.
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
 - SetColorProfileElementSize
f1_keywords:
 - SetColorProfileElementSize
 - icm/SetColorProfileElementSize
dev_langs:
 - c++
---

## -description

Sets the size of a tagged element in an ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param tagType

Identifies the tagged element.

### -param pcbElement

Specifies the size to set the tagged element to. If *cbSize* is zero, this function deletes the specified tagged element. If the tag is a reference, only the tag table entry is deleted, not the data.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

To create a new tagged element in a color profile, use **SetColorProfileElementSize** to set the size, then use [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) to set the element value.

If the specified tag already exists in the profile, **SetColorProfileElementSize** changes the size of the element by truncating it or adding zeroes at the end as the case may be.

If the specified tag already exists and is a reference to another tag, **SetColorProfileElementSize** creates a new data area for the tag that is not shared.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [SetColorProfileElement](/windows/win32/api/icm/nf-icm-setcolorprofileelement)
