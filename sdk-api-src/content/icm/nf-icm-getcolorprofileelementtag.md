---
UID: NF:icm.GetColorProfileElementTag
title: GetColorProfileElementTag
description: Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.
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
 - GetColorProfileElementTag
f1_keywords:
 - GetColorProfileElementTag
 - icm/GetColorProfileElementTag
dev_langs:
 - c++
---

## -description

Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.

## -parameters

### -param hProfile

Specifies a handle to the ICC color profile in question.

### -param dwIndex

Specifies the one-based index of the tag to retrieve.

### -param pTag

Pointer to a variable in which the tag name is to be placed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

This function will fail if *hProfile* is not a valid ICC profile.

**GetColorProfileElementTag** can be used to enumerate all tags in a profile after getting the number of tags in the profile using [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements).

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because profile elements are implicitly associated with, and hard coded to, ICC tag types and there exist many robust XML parsing libraries.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
