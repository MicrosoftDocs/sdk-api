---
UID: NS:mobsync._tagSYNCMGRITEM
title: SYNCMGRITEM (mobsync.h)
description: Provides information about items being enumerated by the ISyncMgrEnumItems interface.
helpviewer_keywords: ["*LPSYNCMGRITEM","LPSYNCMGRITEM","LPSYNCMGRITEM structure pointer [Windows Shell]","SYNCMGRITEM","SYNCMGRITEM structure [Windows Shell]","SYNCMGRITEMSTATE_CHECKED","SYNCMGRITEMSTATE_UNCHECKED","mobsync/LPSYNCMGRITEM","mobsync/SYNCMGRITEM","shell.syncmgr_syncmgritem","syncmgr.syncmgritem"]
old-location: shell\syncmgr_syncmgritem.htm
tech.root: shell
ms.assetid: 84fa1d81-d1b9-44d7-be97-14511ef95528
ms.date: 12/05/2018
ms.keywords: '*LPSYNCMGRITEM, LPSYNCMGRITEM, LPSYNCMGRITEM structure pointer [Windows Shell], SYNCMGRITEM, SYNCMGRITEM structure [Windows Shell], SYNCMGRITEMSTATE_CHECKED, SYNCMGRITEMSTATE_UNCHECKED, mobsync/LPSYNCMGRITEM, mobsync/SYNCMGRITEM, shell.syncmgr_syncmgritem, syncmgr.syncmgritem'
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYNCMGRITEM, *LPSYNCMGRITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSYNCMGRITEM
 - mobsync/_tagSYNCMGRITEM
 - LPSYNCMGRITEM
 - mobsync/LPSYNCMGRITEM
 - SYNCMGRITEM
 - mobsync/SYNCMGRITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRITEM
---

# SYNCMGRITEM structure


## -description

Provides information about items being enumerated by the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure.

### -field dwFlags

Type: <b>DWORD</b>

One or more values from the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgritemflags">SYNCMGRITEMFLAGS</a> enumeration.

### -field ItemID

Type: <b>GUID</b>

The identifier for this item.

### -field dwItemState

Type: <b>DWORD</b>

Indicates whether this item is included in synchronization operations. This member can have one of the following values.



#### SYNCMGRITEMSTATE_UNCHECKED (0)

The default is not including this item in synchronization operations.



#### SYNCMGRITEMSTATE_CHECKED (1)

The default is including this item in synchronization operations.

### -field hIcon

Type: <b>HICON</b>

The icon for this item.

### -field wszItemName

Type: <b>WCHAR[MAX_SYNCMGRITEMNAME]</b>

The name of this item.

### -field ftLastUpdate

Type: <b>FILETIME</b>

The time of the last synchronization for this item.

## -see-also

<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgritemflags">SYNCMGRITEMFLAGS</a>