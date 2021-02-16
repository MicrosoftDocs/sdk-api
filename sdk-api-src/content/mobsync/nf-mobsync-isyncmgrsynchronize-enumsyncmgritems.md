---
UID: NF:mobsync.ISyncMgrSynchronize.EnumSyncMgrItems
title: ISyncMgrSynchronize::EnumSyncMgrItems (mobsync.h)
description: Obtains the ISyncMgrEnumItems interface for the items that are handled by a registered application.
helpviewer_keywords: ["EnumSyncMgrItems","EnumSyncMgrItems method [Windows Shell]","EnumSyncMgrItems method [Windows Shell]","ISyncMgrSynchronize interface","ISyncMgrSynchronize interface [Windows Shell]","EnumSyncMgrItems method","ISyncMgrSynchronize.EnumSyncMgrItems","ISyncMgrSynchronize::EnumSyncMgrItems","mobsync/ISyncMgrSynchronize::EnumSyncMgrItems","shell.syncmgr_isyncmgrsynchronize_enumsyncmgritems","syncmgr.isyncmgrsynchronize_enumsyncmgritems"]
old-location: shell\syncmgr_isyncmgrsynchronize_enumsyncmgritems.htm
tech.root: shell
ms.assetid: 75f6ce68-237f-4228-adcf-f5ec929f49a7
ms.date: 12/05/2018
ms.keywords: EnumSyncMgrItems, EnumSyncMgrItems method [Windows Shell], EnumSyncMgrItems method [Windows Shell],ISyncMgrSynchronize interface, ISyncMgrSynchronize interface [Windows Shell],EnumSyncMgrItems method, ISyncMgrSynchronize.EnumSyncMgrItems, ISyncMgrSynchronize::EnumSyncMgrItems, mobsync/ISyncMgrSynchronize::EnumSyncMgrItems, shell.syncmgr_isyncmgrsynchronize_enumsyncmgritems, syncmgr.isyncmgrsynchronize_enumsyncmgritems
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSynchronize::EnumSyncMgrItems
 - mobsync/ISyncMgrSynchronize::EnumSyncMgrItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.EnumSyncMgrItems
---

# ISyncMgrSynchronize::EnumSyncMgrItems


## -description

Obtains the 
<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface for the items that are handled by a registered application.

## -parameters

### -param ppSyncMgrEnumItems [out]

Type: <b><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a>**</b>

The address of the variable that receives a pointer to a valid 
<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The enumeration interface is returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_MISSINGITEMS</b></dt>
</dl>
</td>
<td width="60%">
The enumeration interface object is returned successfully, but some items are missing. When this success code is returned, the synchronization manager does not remove any stored preferences for ItemIds that are not returned in the enumerator.

</td>
</tr>
</table>

## -remarks

The enumeration object that this method creates implements the 
<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface, which is a standard enumeration interface that contains the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrenumitems-next">Next</a>, <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrenumitems-reset">Reset</a>, <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrenumitems-clone">Clone</a>, and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrenumitems-skip">Skip</a> methods.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>