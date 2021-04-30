---
UID: NF:icm.SetColorProfileHeader
title: SetColorProfileHeader
description: Sets the header data in a specified ICC color profile.
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
 - SetColorProfileHeader
f1_keywords:
 - SetColorProfileHeader
 - icm/SetColorProfileHeader
dev_langs:
 - c++
---

## -description

Sets the header data in a specified ICC color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param pHeader

Pointer to the profile header data to write to the specified profile.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

If the color profile was not opened with read/write permission, **SetColorProfileHeader** fails.

**SetColorProfileHeader** overwrites the current header in the ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [PROFILEHEADER](/windows/win32/api/icm/ns-icm-profileheader)
