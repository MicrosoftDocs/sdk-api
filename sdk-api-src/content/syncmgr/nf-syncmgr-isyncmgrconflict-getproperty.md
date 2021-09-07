---
UID: NF:syncmgr.ISyncMgrConflict.GetProperty
title: ISyncMgrConflict::GetProperty (syncmgr.h)
description: Gets a conflict property, given a property key.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Shell]","GetProperty method [Windows Shell]","ISyncMgrConflict interface","ISyncMgrConflict interface [Windows Shell]","GetProperty method","ISyncMgrConflict.GetProperty","ISyncMgrConflict::GetProperty","PKEY_DateModified","PKEY_ItemNameDisplay","PKEY_Sync_ConflictDescription","PKEY_Sync_HandlerID","PKEY_Sync_ItemID","_shell_ISyncMgrConflict_GetProperty","shell.ISyncMgrConflict_GetProperty","syncmgr/ISyncMgrConflict::GetProperty"]
old-location: shell\ISyncMgrConflict_GetProperty.htm
tech.root: shell
ms.assetid: 8b7b23e7-fbd4-4ced-9610-d001a2167bae
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Shell], GetProperty method [Windows Shell],ISyncMgrConflict interface, ISyncMgrConflict interface [Windows Shell],GetProperty method, ISyncMgrConflict.GetProperty, ISyncMgrConflict::GetProperty, PKEY_DateModified, PKEY_ItemNameDisplay, PKEY_Sync_ConflictDescription, PKEY_Sync_HandlerID, PKEY_Sync_ItemID, _shell_ISyncMgrConflict_GetProperty, shell.ISyncMgrConflict_GetProperty, syncmgr/ISyncMgrConflict::GetProperty
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrConflict::GetProperty
 - syncmgr/ISyncMgrConflict::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflict.GetProperty
---

# ISyncMgrConflict::GetProperty


## -description

Gets a conflict property, given a property key.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the property key for which the property is being requested. Any property key is valid here, including but not limited to the following values.



#### PKEY_ItemNameDisplay

Name of the conflict.



#### PKEY_Sync_ConflictDescription

Summary of the conflict.



#### PKEY_Sync_HandlerID

Sync handler that created the conflict.



#### PKEY_Sync_ItemID

Sync item that created the conflict.



#### PKEY_DateModified

Time the conflict was detected.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this method returns, contains a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the requested property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The properties returned are properties of the conflict and not of the <b>IShellItems</b> that are in conflict.

If the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> referenced in <i>propkey</i> is not present in the property store, this method returns S_OK and the <b>vt</b> member of the structure pointed to by <i>ppropvar</i> is set to VT_EMPTY.