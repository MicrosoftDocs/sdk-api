---
UID: NF:mobsync.ISyncMgrEnumItems.Clone
title: ISyncMgrEnumItems::Clone (mobsync.h)
description: Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","ISyncMgrEnumItems interface","ISyncMgrEnumItems interface [Windows Shell]","Clone method","ISyncMgrEnumItems.Clone","ISyncMgrEnumItems::Clone","mobsync/ISyncMgrEnumItems::Clone","shell.syncmgr_isyncmgrenumitems_clone","syncmgr.isyncmgrenumitems_clone"]
old-location: shell\syncmgr_isyncmgrenumitems_clone.htm
tech.root: shell
ms.assetid: 33bf4956-3d16-412c-9551-4ae3366ddd78
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],ISyncMgrEnumItems interface, ISyncMgrEnumItems interface [Windows Shell],Clone method, ISyncMgrEnumItems.Clone, ISyncMgrEnumItems::Clone, mobsync/ISyncMgrEnumItems::Clone, shell.syncmgr_isyncmgrenumitems_clone, syncmgr.isyncmgrenumitems_clone
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
 - ISyncMgrEnumItems::Clone
 - mobsync/ISyncMgrEnumItems::Clone
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
 - ISyncMgrEnumItems.Clone
---

# ISyncMgrEnumItems::Clone


## -description

Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.

## -parameters

### -param ppenum [out]

Type: <b>ppenum**</b>

The address of a variable that receives the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems">ISyncMgrEnumItems</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

Return S_OK if the method succeeds.

## -remarks

The calling application must release the new enumerator separately from the first enumerator.