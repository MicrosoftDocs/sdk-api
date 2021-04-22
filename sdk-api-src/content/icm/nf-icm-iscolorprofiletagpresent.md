---
UID: NF:icm.IsColorProfileTagPresent
title: IsColorProfileTagPresent
description: Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.
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
 - IsColorProfileTagPresent
f1_keywords:
 - IsColorProfileTagPresent
 - icm/IsColorProfileTagPresent
dev_langs:
 - c++
---

## -description

Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.

## -parameters

### -param hProfile

Specifies a handle to the ICC profile in question.

### -param tag

Specifies the ICC tag to check.

### -param pbPresent

Pointer to a variable that is set to **TRUE** on return if the specified ICC tag is present, or **FALSE** if not.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with and hard coded to ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
