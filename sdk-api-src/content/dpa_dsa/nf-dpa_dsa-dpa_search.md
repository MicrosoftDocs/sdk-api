---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DPA_Search function


## -description


<p class="CCE_Message">[<b>DPA_Search</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Finds an item in a dynamic pointer array (DPA).


## -parameters




### -param hdpa

TBD


### -param pFind

Type: <b>void*</b>

A pointer to search for.


### -param iStart

Type: <b>int</b>

The index at which to start search.


### -param pfnCompare

TBD


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.


### -param options

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This parameter may be one or more of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPAS_SORTED"></a><a id="dpas_sorted"></a><dl>
<dt><b>DPAS_SORTED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the DPA is sorted.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTBEFORE"></a><a id="dpas_insertbefore"></a><dl>
<dt><b>DPAS_INSERTBEFORE</b></dt>
</dl>
</td>
<td width="60%">
This value is only valid in conjunction with DPAS_SORTED. If the item is not found, return the position where the item is expected to be found in the sorted DPA.

</td>
</tr>
<tr>
<td width="40%"><a id="DPAS_INSERTAFTER"></a><a id="dpas_insertafter"></a><dl>
<dt><b>DPAS_INSERTAFTER</b></dt>
</dl>
</td>
<td width="60%">
This value is only valid in conjunction with DPAS_SORTED. If the item is not found, return the position where the item is expected to be found in the sorted DPA.

</td>
</tr>
</table>
 


#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


#### - pfnCmp

Type: <b><a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a></b>

A comparison function pointer. See <a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a> for the comparison function prototype.


## -returns



Type: <b>int</b>

Returns the index where the item was found in the DPA or <code>-1</code> if the item was not found.



