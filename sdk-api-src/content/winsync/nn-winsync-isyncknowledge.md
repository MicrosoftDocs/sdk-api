---
UID: NN:winsync.ISyncKnowledge
title: ISyncKnowledge (winsync.h)
description: Represents knowledge that a replica has about its item store.
helpviewer_keywords: ["ISyncKnowledge","ISyncKnowledge interface [Windows Sync]","ISyncKnowledge interface [Windows Sync]","described","winsync.isyncknowledge","winsync/ISyncKnowledge"]
old-location: winsync\isyncknowledge.htm
tech.root: winsync
ms.assetid: cfb08476-7b5d-4953-b723-5160330e57be
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge, ISyncKnowledge interface [Windows Sync], ISyncKnowledge interface [Windows Sync],described, winsync.isyncknowledge, winsync/ISyncKnowledge
f1_keywords:
- winsync/ISyncKnowledge
dev_langs:
- c++
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winsync.h
api_name:
- ISyncKnowledge
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge interface


## -description


Represents knowledge that a replica has about its item store.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncKnowledge</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncKnowledge</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncKnowledge</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of this object, and copies the data from this object to the new object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containschange">ContainsChange</a>
</td>
<td align="left" width="63%">
Indicates whether the specified item change is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containschangeunit">ContainsChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates whether the specified change unit change is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containsknowledge">ContainsKnowledge</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge is known by this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-convertversion">ConvertVersion</a>
</td>
<td align="left" width="63%">
Converts a version from another replica into one that is compatible with the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-excludechangeunit">ExcludeChangeUnit</a>
</td>
<td align="left" width="63%">
Removes knowledge about the specified change unit from the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-excludeitem">ExcludeItem</a>
</td>
<td align="left" width="63%">
Removes knowledge about the specified item from the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-findclockvectorforchangeunit">FindClockVectorForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the specified change unit ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-findclockvectorforitem">FindClockVectorForItem</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the specified item ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-findmintickcountforreplica">FindMinTickCountForReplica</a>
</td>
<td align="left" width="63%">
Finds the minimum tick count in the knowledge for the specified replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getchangeunitexceptions">GetChangeUnitExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>IChangeUnitException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getownerreplicaid">GetOwnerReplicaId</a>
</td>
<td align="left" width="63%">
Gets the ID of the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getrangeexceptions">GetRangeExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>IRangeException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getreplicakeymap">GetReplicaKeyMap</a>
</td>
<td align="left" width="63%">
Gets the <b>IReplicaKeyMap</b> object that is associated with this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getscopevector">GetScopeVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that defines the changes that are contained in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getsingleitemexceptions">GetSingleItemExceptions</a>
</td>
<td align="left" width="63%">
Gets an object that can enumerate the <b>ISingleItemException</b> objects that are stored in the knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the version of this knowledge structure.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-mapremotetolocal">MapRemoteToLocal</a>
</td>
<td align="left" width="63%">
Converts a knowledge object from another replica into one that is compatible with the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontochangeunit">ProjectOntoChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified change unit.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontoitem">ProjectOntoItem</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified item.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontorange">ProjectOntoRange</a>
</td>
<td align="left" width="63%">
Gets the knowledge for the specified range of item IDs.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the knowledge object data to a byte array.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-setlocaltickcount">SetLocalTickCount</a>
</td>
<td align="left" width="63%">
Sets the tick count for the replica that owns this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-union">Union</a>
</td>
<td align="left" width="63%">
Combines the specified knowledge with the current knowledge.


</td>
</tr>
</table> 


## -remarks



Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from knowledge inspection methods, such as <b>GetScopeVector</b>, <b>GetRangeExceptions</b>, <b>GetSingleItemExceptions</b>, <b>GetChangeUnitExceptions</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitexception">IChangeUnitException Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-irangeexception">IRangeException Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isingleitemexception">ISingleItemException Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

