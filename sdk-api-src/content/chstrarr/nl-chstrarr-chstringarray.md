---
UID: NL:chstrarr.CHStringArray
title: CHStringArray (chstrarr.h)
description: The following table lists the CHStringArray methods and operators.
helpviewer_keywords: ["??1CHStringArray@@QAE@XZ","??1CHStringArray@@QEAA@XZ","CHStringArray","CHStringArray class [Windows Management Instrumentation]","CHStringArray class [Windows Management Instrumentation]","described","_hmm_chstringarray","chstrarr/CHStringArray","wmi.chstringarray"]
old-location: wmi\chstringarray.htm
tech.root: wmi
ms.assetid: 62959345-4fed-4107-b155-1746ad35c658
ms.date: 12/05/2018
ms.keywords: ??1CHStringArray@@QAE@XZ, ??1CHStringArray@@QEAA@XZ, CHStringArray, CHStringArray class [Windows Management Instrumentation], CHStringArray class [Windows Management Instrumentation],described, _hmm_chstringarray, chstrarr/CHStringArray, wmi.chstringarray
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
 - CHStringArray
 - chstrarr/CHStringArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray
 - ??1CHStringArray@@QAE@XZ
 - ??1CHStringArray@@QEAA@XZ
---

# CHStringArray class


## -description

<p class="CCE_Message">[The <b>CHStringArray</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The following table lists the <b>CHStringArray</b> methods and operators.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CHStringArray</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CHStringArray</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-chstringarray">CHStringArray</a>
</td>
<td align="left" width="63%">
Constructs an empty array for <a href="/windows/desktop/WmiSdk/chstring">CHString</a> objects.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CHStringArray</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">Add</a>
</td>
<td align="left" width="63%">
Adds an element to the end of the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-append">Append</a>
</td>
<td align="left" width="63%">
Appends another array to the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-copy">Copy</a>
</td>
<td align="left" width="63%">
Copies another array to the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-elementat(int)">ElementAt</a>
</td>
<td align="left" width="63%">
Returns a temporary reference to the element pointer within the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-freeextra">FreeExtra</a>
</td>
<td align="left" width="63%">
Frees all unused memory above the current upper bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">GetAt</a>
</td>
<td align="left" width="63%">
Returns the value at a given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">GetData</a>
</td>
<td align="left" width="63%">
Allows access to elements in the array. The value can be <b>NULL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>
</td>
<td align="left" width="63%">
Returns the largest valid index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)">InsertAt</a>
</td>
<td align="left" width="63%">Overloaded. Inserts an element (or all of the elements in another array) at a specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/WmiSdk/chstringarray--operator-brackets">Operator []</a>
</td>
<td align="left" width="63%">
Sets or gets the element at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all of the elements from this array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes an element at a specific index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">SetAt</a>
</td>
<td align="left" width="63%">
Sets the value for a given index; the array is not allowed to grow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setatgrow">SetAtGrow</a>
</td>
<td align="left" width="63%">
Sets the value for a given index; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Sets the number of elements to be contained in this array

</td>
</tr>
</table>