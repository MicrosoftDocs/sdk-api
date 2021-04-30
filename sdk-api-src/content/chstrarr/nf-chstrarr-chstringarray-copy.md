---
UID: NF:chstrarr.CHStringArray.Copy
title: CHStringArray::Copy (chstrarr.h)
description: The Copy method overwrites the elements of the given array with the elements of another array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","Copy method","CHStringArray.Copy","CHStringArray::Copy","Copy","Copy method [Windows Management Instrumentation]","Copy method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_copy","chstrarr/CHStringArray::Copy","wmi.chstringarray_copy"]
old-location: wmi\chstringarray_copy.htm
tech.root: wmi
ms.assetid: 9598340f-c315-4c93-bc8a-2b7c1eaf5a35
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],Copy method, CHStringArray.Copy, CHStringArray::Copy, Copy, Copy method [Windows Management Instrumentation], Copy method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_copy, chstrarr/CHStringArray::Copy, wmi.chstringarray_copy
req.header: chstrarr.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHStringArray::Copy
 - chstrarr/CHStringArray::Copy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.Copy
---

# CHStringArray::Copy


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Copy</b> method overwrites the elements of the given array with the elements of another array.

## -parameters

### -param src [ref]

Source of the elements to be copied to the array.

## -returns

This method does not return a value.

## -remarks

The <b>Copy</b> method does not free memory, but it allocates extra memory to accommodate the elements copied to the array.


#### Examples

The following code example shows the use of <b>CHStringArray::Copy</b>.


```cpp
CHStringArray a1, a2;
int idx, size;

a1.Add( L"String 1" );
a1.Add( L"String 2" );
a2.Add( L"String 5" );

size = a1.GetSize();
for (idx=0; idx<size; idx++)
   printf("[%d]: %S\n", idx, a1[idx]);

a1.Copy(a2);
size = a1.GetSize();
for (idx=0; idx<size; idx++)
   printf("[%d]: %S\n", idx, a1[idx]);
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-append">CHStringArray::Append</a>