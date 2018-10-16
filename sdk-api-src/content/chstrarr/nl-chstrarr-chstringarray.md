---
UID: NL:chstrarr.CHStringArray
title: CHStringArray
author: windows-sdk-content
description: The following table lists the CHStringArray methods and operators.
old-location: wmi\chstringarray.htm
tech.root: WmiSdk
ms.assetid: 62959345-4fed-4107-b155-1746ad35c658
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "??1CHStringArray@@QAE@XZ, ??1CHStringArray@@QEAA@XZ, CHStringArray, CHStringArray class [Windows Management Instrumentation], CHStringArray class [Windows Management Instrumentation],described, _hmm_chstringarray, chstrarr/CHStringArray, wmi.chstringarray"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
 - CHStringArray
 - ??1CHStringArray@@QAE@XZ
 - ??1CHStringArray@@QEAA@XZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHStringArray class


## -description


<p class="CCE_Message">[The <b>CHStringArray</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
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
<a href="https://msdn.microsoft.com/b20e3476-7caa-4fcf-98cc-44ffafafe94a">CHStringArray</a>
</td>
<td align="left" width="63%">
Constructs an empty array for <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> objects.

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
<a href="https://msdn.microsoft.com/f5a0b8e6-b40a-4dc7-bf36-ec629e2899db">Add</a>
</td>
<td align="left" width="63%">
Adds an element to the end of the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c37df3d4-9b0b-4ed3-ab51-407f26203578">Append</a>
</td>
<td align="left" width="63%">
Appends another array to the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9598340f-c315-4c93-bc8a-2b7c1eaf5a35">Copy</a>
</td>
<td align="left" width="63%">
Copies another array to the array; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5431a9ae-e009-4457-87e4-bb91da8bfdb6">ElementAt</a>
</td>
<td align="left" width="63%">
Returns a temporary reference to the element pointer within the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ed54cc4-284b-4cd7-80c1-e9c5ff27c4bf">FreeExtra</a>
</td>
<td align="left" width="63%">
Frees all unused memory above the current upper bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a950bc1e-1c13-4880-aee7-9a4606979993">GetAt</a>
</td>
<td align="left" width="63%">
Returns the value at a given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b59a0c42-e753-43ff-bf39-279f0a8b9d2b">GetData</a>
</td>
<td align="left" width="63%">
Allows access to elements in the array. The value can be <b>NULL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5db50c38-a9c7-4711-925e-291cebf2b6f1">GetSize</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c200f9-c63b-4842-881f-5c077e4618b8">GetUpperBound</a>
</td>
<td align="left" width="63%">
Returns the largest valid index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d6355bc-7df2-4aa3-8e47-0239d726ed7d">InsertAt</a>
</td>
<td align="left" width="63%">Overloaded. Inserts an element (or all of the elements in another array) at a specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93b10bef-908e-4c5e-aac3-b13051b2e7c9">Operator []</a>
</td>
<td align="left" width="63%">
Sets or gets the element at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be9df3fd-afa5-4f07-99cd-ddccdeaa3fd3">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all of the elements from this array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7555074-4f9a-46be-b321-f16e00663c32">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes an element at a specific index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/709bed59-c154-4103-9d38-398945657ec6">SetAt</a>
</td>
<td align="left" width="63%">
Sets the value for a given index; the array is not allowed to grow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49cc7e6f-2d15-4756-bffd-e21f38b8ce8b">SetAtGrow</a>
</td>
<td align="left" width="63%">
Sets the value for a given index; the array grows if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9320b6b6-5253-419e-a293-3b9d030f5963">SetSize</a>
</td>
<td align="left" width="63%">
Sets the number of elements to be contained in this array

</td>
</tr>
</table> 

