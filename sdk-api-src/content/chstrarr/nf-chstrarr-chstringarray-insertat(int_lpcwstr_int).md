---
UID: NF:chstrarr.CHStringArray.InsertAt(int,LPCWSTR,int)
title: CHStringArray::InsertAt (chstrarr.h)
description: The InsertAt method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.
helpviewer_keywords: ["CHStringArray.InsertAt","CHStringArray::InsertAt","CHStringArray::InsertAt methods [Windows Management Instrumentation]","InsertAt","chstrarr/CHStringArray::InsertAt","wmi.insertat_method_in_class_chstringarray"]
old-location: wmi\insertat_method_in_class_chstringarray.htm
tech.root: wmi
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.date: 12/05/2018
ms.keywords: CHStringArray.InsertAt, CHStringArray::InsertAt, CHStringArray::InsertAt methods [Windows Management Instrumentation], InsertAt, chstrarr/CHStringArray::InsertAt, wmi.insertat_method_in_class_chstringarray
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
 - CHStringArray::InsertAt
 - chstrarr/CHStringArray::InsertAt
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
 - CHStringArray::InsertAt
---

# CHStringArray::InsertAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]
<span>The <b>InsertAt</b> method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa385383(v=vs.85)">InsertAt(int,LPCWSTR,int)</a>
</td>
<td align="left" width="63%">
Inserts one or more elements at a specified index in an array.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)">InsertAt(int,CHStringArray*)</a>
</td>
<td align="left" width="63%">
Inserts all the elements of another <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> at a specified index in an array.

</td>
</tr>
</table>

## -parameters

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>