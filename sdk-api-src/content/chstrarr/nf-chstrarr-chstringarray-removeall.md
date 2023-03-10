---
UID: NF:chstrarr.CHStringArray.RemoveAll
title: CHStringArray::RemoveAll (chstrarr.h)
description: The RemoveAll method removes all the CHString members from this array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","RemoveAll method","CHStringArray.RemoveAll","CHStringArray::RemoveAll","RemoveAll","RemoveAll method [Windows Management Instrumentation]","RemoveAll method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_removeall","chstrarr/CHStringArray::RemoveAll","wmi.chstringarray_removeall"]
old-location: wmi\chstringarray_removeall.htm
tech.root: wmi
ms.assetid: be9df3fd-afa5-4f07-99cd-ddccdeaa3fd3
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAll method, CHStringArray.RemoveAll, CHStringArray::RemoveAll, RemoveAll, RemoveAll method [Windows Management Instrumentation], RemoveAll method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeall, chstrarr/CHStringArray::RemoveAll, wmi.chstringarray_removeall
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
 - CHStringArray::RemoveAll
 - chstrarr/CHStringArray::RemoveAll
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
 - CHStringArray.RemoveAll
---

# CHStringArray::RemoveAll


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAll</b> method removes all the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> members from this array.



## -remarks

The <b>RemoveAll</b> method works on empty arrays.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAll</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1 
assert( array.GetSize() == 2 ); 
array.RemoveAll(); 
assert( array.GetSize() == 0 );
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-freeextra">CHStringArray::FreeExtra</a>
