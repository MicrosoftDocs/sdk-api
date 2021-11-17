---
UID: NL:refptrco.TRefPointerCollection
title: TRefPointerCollection (refptrco.h)
description: The TRefPointerCollection class is a container class that collects pointers to objects. These pointers can be enumerated.
helpviewer_keywords: ["TRefPointerCollection","TRefPointerCollection class [Windows Management Instrumentation]","TRefPointerCollection class [Windows Management Instrumentation]","described","_hmm_trefpointercollection","refptrco/TRefPointerCollection","wmi.trefpointercollection"]
old-location: wmi\trefpointercollection.htm
tech.root: wmi
ms.assetid: a2d1758a-4a7e-40fd-84c7-a25bc36ab538
ms.date: 12/05/2018
ms.keywords: TRefPointerCollection, TRefPointerCollection class [Windows Management Instrumentation], TRefPointerCollection class [Windows Management Instrumentation],described, _hmm_trefpointercollection, refptrco/TRefPointerCollection, wmi.trefpointercollection
req.header: refptrco.h
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
 - TRefPointerCollection
 - refptrco/TRefPointerCollection
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
 - TRefPointerCollection
---

# TRefPointerCollection class


## -description

<p class="CCE_Message">[The <b>TRefPointerCollection</b> 
    class is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>TRefPointerCollection</b> class is a container 
    class that collects pointers to objects. These pointers can be enumerated.

<b>TRefPointerCollection</b> has these types of members:
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to a collection and calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> 
     method to increment the reference count.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-beginenum">BeginEnum</a>
</td>
<td align="left" width="63%">
Begins an enumeration of a collection. Call this method with the cursor to be initialized as a parameter 
     before enumerating the collection (REFPTRCOLLECTION_POSITION).

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-empty">Empty</a>
</td>
<td align="left" width="63%">
Empties out the list, releasing all held pointers.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-endenum">EndEnum</a>
</td>
<td align="left" width="63%">
Ends enumeration of a collection. Call this method when the enumerating operation is finished.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-getnext">GetNext</a>
</td>
<td align="left" width="63%">
Gets next item from the list and calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> 
     method to increment the reference count. (The user must release the pointer when done and pass in the same cursor 
     each time.)

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Returns the number of items in the list.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-trefpointercollection(consttrefpointercollection_)">TRefPointerCollection</a>
</td>
<td align="left" width="63%">
Constructs a new <b>TRefPointerCollection</b> object.

</td>
</tr>
</table>

## -remarks

The destructor for this class is <b>TRefPointerCollection::~TRefPointerCollection</b>.
