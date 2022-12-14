---
UID: NF:propsys.IPersistSerializedPropStorage.SetFlags
title: IPersistSerializedPropStorage::SetFlags (propsys.h)
description: Toggles the property store object between the read-only and read/write state.
helpviewer_keywords: ["FPSPS_DEFAULT","FPSPS_READONLY","FPSPS_TREAT_NEW_VALUES_AS_DIRTY","IPersistSerializedPropStorage interface [Windows Shell]","SetFlags method","IPersistSerializedPropStorage.SetFlags","IPersistSerializedPropStorage::SetFlags","SetFlags","SetFlags method [Windows Shell]","SetFlags method [Windows Shell]","IPersistSerializedPropStorage interface","_shell_IPersistSerializedPropStorage_SetFlags","propsys/IPersistSerializedPropStorage::SetFlags","shell.IPersistSerializedPropStorage_SetFlags"]
old-location: shell\IPersistSerializedPropStorage_SetFlags.htm
tech.root: shell
ms.assetid: df7a817e-de81-4e27-ab37-192e668bf7fa
ms.date: 12/05/2018
ms.keywords: FPSPS_DEFAULT, FPSPS_READONLY, FPSPS_TREAT_NEW_VALUES_AS_DIRTY, IPersistSerializedPropStorage interface [Windows Shell],SetFlags method, IPersistSerializedPropStorage.SetFlags, IPersistSerializedPropStorage::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IPersistSerializedPropStorage interface, _shell_IPersistSerializedPropStorage_SetFlags, propsys/IPersistSerializedPropStorage::SetFlags, shell.IPersistSerializedPropStorage_SetFlags
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPersistSerializedPropStorage::SetFlags
 - propsys/IPersistSerializedPropStorage::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPersistSerializedPropStorage.SetFlags
---

# IPersistSerializedPropStorage::SetFlags


## -description

Toggles the property store object between the read-only and read/write state.

## -parameters

### -param flags [in]

Type: <b>PERSIST_SPROPSTORE_FLAGS</b>

The <i>flags</i> parameter takes one of the following values to set options for the behavior of the property storage:



#### FPSPS_DEFAULT (0x00000000)

<b>Windows 7 and later</b>. The property store object is read/write.



#### FPSPS_READONLY (0x00000001)

The property store object is read-only.



#### FPSPS_TREAT_NEW_VALUES_AS_DIRTY (0x00000002)

<b>Introduced in Windows 8</b>. New property values that are added to the property store through the <a href="/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)">IPropertyStore::SetValue</a> method will cause the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-isdirty">IPersistStream::IsDirty</a> method to return S_OK. If this flag is not set, the addition of new property values to the property store does not affect the value returned by <b>IPersistStream::IsDirty</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Read/write is the default setting. <b>IPersistSerializedPropStorage::SetFlags</b> can be called at any time to toggle the read-only and read/write state of the property store.

In versions of Windows before Windows 7, callers can assign a literal zero value directly into the <i>flags</i> parameter to set the read/write state. As of Windows 7, the FPSPS_DEFAULT flag value should be used instead.