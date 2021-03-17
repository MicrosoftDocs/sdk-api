---
UID: NF:chstrarr.CHStringArray.Add
title: CHStringArray::Add (chstrarr.h)
description: The Add method adds a new element to the end of an array, increasing the array by one.
helpviewer_keywords: ["?Add@CHStringArray@@QAEHPBG@Z","?Add@CHStringArray@@QEAAHPEBG@Z","Add","Add method [Windows Management Instrumentation]","Add method [Windows Management Instrumentation]","CHStringArray interface","CHStringArray interface [Windows Management Instrumentation]","Add method","CHStringArray.Add","CHStringArray::Add","_hmm_chstringarray_add","chstrarr/CHStringArray::Add","wmi.chstringarray_add"]
old-location: wmi\chstringarray_add.htm
tech.root: wmi
ms.assetid: f5a0b8e6-b40a-4dc7-bf36-ec629e2899db
ms.date: 12/05/2018
ms.keywords: ?Add@CHStringArray@@QAEHPBG@Z, ?Add@CHStringArray@@QEAAHPEBG@Z, Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],CHStringArray interface, CHStringArray interface [Windows Management Instrumentation],Add method, CHStringArray.Add, CHStringArray::Add, _hmm_chstringarray_add, chstrarr/CHStringArray::Add, wmi.chstringarray_add
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
 - CHStringArray::Add
 - chstrarr/CHStringArray::Add
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
 - CHStringArray.Add
 - ?Add@CHStringArray@@QAEHPBG@Z
 - ?Add@CHStringArray@@QEAAHPEBG@Z
---

# CHStringArray::Add


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Add</b> method adds a new element to the end of an 
    array, increasing the array by one.

## -parameters

### -param newElement

The element to be added to the array.

## -returns

If the <b>Add</b> method is successful, it returns the 
       index of the added element.

## -remarks

If <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setsize">SetSize</a> has been used with an nGrowBy value 
    greater than 1, then extra memory can be allocated. However, the upper bound increases by only one.


#### Examples

The following code example shows the use of 
     <b>Add</b>.


```cpp
    CHStringArray array;
    CHString s( L"String 2");
    
    array.Add( L"String 1" ); // Element 0
    array.Add( s );           // Element 1
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-append">CHStringArray::Append</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-copy">CHStringArray::Copy</a>