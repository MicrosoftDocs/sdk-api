---
UID: NF:icm.SetColorProfileElementReference
title: SetColorProfileElementReference
description: Creates in a specified ICC color profile a new tag that references the same data as an existing tag.
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
 - SetColorProfileElementReference
f1_keywords:
 - SetColorProfileElementReference
 - icm/SetColorProfileElementReference
dev_langs:
 - c++
---

## -description

Creates in a specified ICC color profile a new tag that references the same data as an existing tag.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param newTag

Identifies the new tag to create.

### -param refTag

Identifies the existing tag whose data is to be referenced by the new tag.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

If *newTag* already exists or *refTag* does not exist, **SetColorProfileElementReference** fails.

If the color profile was not opened with read/write permission, **SetColorProfileElementReference** fails.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
