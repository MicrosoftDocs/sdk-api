---
UID: NF:chstrarr.CHStringArray.ElementAt(int)~r1
title: CHStringArray::ElementAt (chstrarr.h)
description: The ElementAt method returns a temporary reference to the element pointer within the array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","ElementAt method","CHStringArray.ElementAt","CHStringArray::ElementAt","ElementAt","ElementAt method [Windows Management Instrumentation]","ElementAt method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_elementat","chstrarr/CHStringArray::ElementAt","wmi.chstringarray_elementat"]
old-location: wmi\chstringarray_elementat.htm
tech.root: wmi
ms.assetid: 5431a9ae-e009-4457-87e4-bb91da8bfdb6
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],ElementAt method, CHStringArray.ElementAt, CHStringArray::ElementAt, ElementAt, ElementAt method [Windows Management Instrumentation], ElementAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_elementat, chstrarr/CHStringArray::ElementAt, wmi.chstringarray_elementat
f1_keywords:
- chstrarr/CHStringArray.ElementAt
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CHStringArray.ElementAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHStringArray::ElementAt


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ElementAt</b> method returns a temporary reference to the element pointer within the array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.


## -returns



If the <b>ElementAt</b> method is successful, it returns a reference to the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string at the <i>nIndex</i> position in the <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> array.




## -remarks



Use the <b>ElementAt</b> method to implement the left-side assignment operator for arrays. This is an advanced method, which you should use only to implement special array operators.


#### Examples

See the example for <a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">CHStringArray::GetSize</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">CHStringArray::GetAt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">CHStringArray::GetData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">CHStringArray::SetAt</a>
 

 

