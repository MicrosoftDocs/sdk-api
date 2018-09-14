---
UID: NN:mobsync.ISyncMgrEnumItems
title: ISyncMgrEnumItems
author: windows-sdk-content
description: Exposes methods that enumerate through an array of SYNCMGRITEM structures.
old-location: shell\syncmgr_isyncmgrenumitems.htm
tech.root: shell
ms.assetid: d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ISyncMgrEnumItems, ISyncMgrEnumItems interface [Windows Shell], ISyncMgrEnumItems interface [Windows Shell],described, mobsync/ISyncMgrEnumItems, shell.syncmgr_isyncmgrenumitems, syncmgr.isyncmgrenumitems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrEnumItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrEnumItems interface


## -description


Exposes methods that enumerate through an array of <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structures. Each of these structures provides information about an item that can be synchronized. <b>ISyncMgrEnumItems</b> has the same methods as all standard enumerator interfaces: Next, Skip, Reset, and Clone.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEnumItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrEnumItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrEnumItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33bf4956-3d16-412c-9551-4ae3366ddd78">Clone</a>
</td>
<td align="left" width="63%">
Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb4ab08a-aa12-46f0-8c7d-82742b0b1538">Next</a>
</td>
<td align="left" width="63%">
Enumerates the next <i>celt</i> elements in the enumerator's list, returning them in <i>rgelt</i> along with the actual number of enumerated elements in <i>pceltFetched</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91265648-1294-423d-8e09-6d14eb0b6d9e">Reset</a>
</td>
<td align="left" width="63%">
Instructs the enumerator to position itself at the beginning of the list of elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f317306b-5317-4c5e-a5e6-fd2d8728bc52">Skip</a>
</td>
<td align="left" width="63%">
Instructs the enumerator to skip the next <i>celt</i> elements in the enumeration so that the next call to <a href="https://msdn.microsoft.com/bb4ab08a-aa12-46f0-8c7d-82742b0b1538">ISyncMgrEnumItems::Next</a> does not return those elements.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
If the registered application works with the synchronization manager to synchronize items, it must implement an enumerator object with this interface to enumerate through the items.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The synchronization manager obtains a pointer to this interface and calls each method during the synchronization process.




## -see-also




<a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a>
 

 

