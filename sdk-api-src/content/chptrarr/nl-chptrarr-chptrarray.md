---
UID: NL:chptrarr.CHPtrArray
title: CHPtrArray
author: windows-sdk-content
description: The CHPtrArray class is part of the WMI Provider Framework. CHPtrArray is a utility interface for array pointer management used for provider handling of WMI queries.
old-location: wmi\chptrarray.htm
old-project: WmiSdk
ms.assetid: 507c8262-c5e8-470e-be89-566ae732946d
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "??1CHPtrArray@@QAE@XZ, CHPtrArray, CHPtrArray class [Windows Management Instrumentation], CHPtrArray class [Windows Management Instrumentation],described, chptrarr/CHPtrArray, wmi.chptrarray"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: chptrarr.h
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
tech.root: 
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHPtrArray
 - ??1CHPtrArray@@QAE@XZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHPtrArray class


## -description


<p class="CCE_Message">[The <b>CHPtrArray</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CHPtrArray</b> class is part of the WMI Provider Framework. <b>CHPtrArray</b> is a utility interface for array pointer management used for provider handling of WMI queries.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CHPtrArray</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Operators</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CHPtrArray</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9435d0e6-bb26-40a9-a13f-a744588cc0b0">CHPtrArray</a>
</td>
<td align="left" width="63%">
Constructor.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CHPtrArray</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Accesses an element in a <b>CHPtrArray</b> array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b9bcd3f-06d9-47f1-aecb-1c611c9866bd">GetSize</a>
</td>
<td align="left" width="63%">
Obtains the pointer array size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51de0ff1-e8e9-4484-80d6-51179ef82a51">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all the <b>CHPtrArray</b> members from this array.

</td>
</tr>
</table> 
<h3><a id="operators"></a>Operators</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CHPtrArray</b> class has these operators.
<table>
<tr>
<th align="left" width="37%">Operator</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544338">operator[]</a>
</td>
<td align="left" width="63%">
Gets the element at the specified index.

</td>
</tr>
</table> 


## -remarks



The destructor for the class is <b>CHPtrArray::~CHPtrArray</b>.




## -see-also




<a href="https://msdn.microsoft.com/d2414a72-3435-4035-bcd9-b3ec87f5709c">Provider Framework Utility Classes</a>
 

 

