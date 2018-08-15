---
UID: NL:refptrco.TRefPointerCollection
title: TRefPointerCollection
author: windows-sdk-content
description: The TRefPointerCollection class is a container class that collects pointers to objects. These pointers can be enumerated.
old-location: wmi\trefpointercollection.htm
old-project: WmiSdk
ms.assetid: a2d1758a-4a7e-40fd-84c7-a25bc36ab538
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: TRefPointerCollection, TRefPointerCollection class [Windows Management Instrumentation], TRefPointerCollection class [Windows Management Instrumentation],described, _hmm_trefpointercollection, refptrco/TRefPointerCollection, wmi.trefpointercollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: refptrco.h
req.include-header: FwCommon.h
req.redist: 
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
req.typenames: RECO_RANGE
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
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# TRefPointerCollection class


## -description


<p class="CCE_Message">[The <b>TRefPointerCollection</b> 
    class is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>TRefPointerCollection</b> class is a container 
    class that collects pointers to objects. These pointers can be enumerated.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">TRefPointerCollection</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>TRefPointerCollection</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/959cd8e7-ea0c-4b98-8e13-398e09c62668">Add</a>
</td>
<td align="left" width="63%">
Adds an item to a collection and calls the <a href="_com_iunknown_addref">AddRef</a> 
     method to increment the reference count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f7879e8-0eeb-4768-a478-8effd4e355d3">BeginEnum</a>
</td>
<td align="left" width="63%">
Begins an enumeration of a collection. Call this method with the cursor to be initialized as a parameter 
     before enumerating the collection (REFPTRCOLLECTION_POSITION).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08f9dcc6-cb85-42aa-837b-ab8021f488c6">Empty</a>
</td>
<td align="left" width="63%">
Empties out the list, releasing all held pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86dcfc2e-fc73-4030-a63f-5284c2123a21">EndEnum</a>
</td>
<td align="left" width="63%">
Ends enumeration of a collection. Call this method when the enumerating operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0dfb2c7-71f6-4870-8018-145e890d4928">GetNext</a>
</td>
<td align="left" width="63%">
Gets next item from the list and calls the <a href="_com_iunknown_addref">AddRef</a> 
     method to increment the reference count. (The user must release the pointer when done and pass in the same cursor 
     each time.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ffdf8b9-53be-4a3d-8272-02f6c3be5fd1">GetSize</a>
</td>
<td align="left" width="63%">
Returns the number of items in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4fcfe31-49ce-434c-a6e4-cf60e0a435e6">TRefPointerCollection</a>
</td>
<td align="left" width="63%">
Constructs a new <b>TRefPointerCollection</b> object.

</td>
</tr>
</table> 


## -remarks



The destructor for this class is <b>TRefPointerCollection::~TRefPointerCollection</b>.



