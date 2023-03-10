---
UID: NF:mobsync.ISyncMgrEnumItems.Skip
title: ISyncMgrEnumItems::Skip (mobsync.h)
description: Instructs the enumerator to skip the next celt elements in the enumeration so that the next call to ISyncMgrEnumItems::Next does not return those elements.
helpviewer_keywords: ["ISyncMgrEnumItems interface [Windows Shell]","Skip method","ISyncMgrEnumItems.Skip","ISyncMgrEnumItems::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","ISyncMgrEnumItems interface","mobsync/ISyncMgrEnumItems::Skip","shell.syncmgr_isyncmgrenumitems_skip","syncmgr.isyncmgrenumitems_skip"]
old-location: shell\syncmgr_isyncmgrenumitems_skip.htm
tech.root: shell
ms.assetid: f317306b-5317-4c5e-a5e6-fd2d8728bc52
ms.date: 12/05/2018
ms.keywords: ISyncMgrEnumItems interface [Windows Shell],Skip method, ISyncMgrEnumItems.Skip, ISyncMgrEnumItems::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],ISyncMgrEnumItems interface, mobsync/ISyncMgrEnumItems::Skip, shell.syncmgr_isyncmgrenumitems_skip, syncmgr.isyncmgrenumitems_skip
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
 - ISyncMgrEnumItems::Skip
 - mobsync/ISyncMgrEnumItems::Skip
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
 - ISyncMgrEnumItems.Skip
---

# ISyncMgrEnumItems::Skip


## -description

Instructs the enumerator to skip the next <i>celt</i> elements in the enumeration so that the next call to <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrenumitems-next">ISyncMgrEnumItems::Next</a> does not return those elements.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.

## -returns

Type: <b>HRESULT</b>

Return S_OK if the method succeeds.