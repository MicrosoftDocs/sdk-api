---
UID: NF:propsys.IPersistSerializedPropStorage.GetPropertyStorage
title: IPersistSerializedPropStorage::GetPropertyStorage (propsys.h)
description: Gets the serialized property storage data from the property store instance.
helpviewer_keywords: ["GetPropertyStorage","GetPropertyStorage method [Windows Shell]","GetPropertyStorage method [Windows Shell]","IPersistSerializedPropStorage interface","IPersistSerializedPropStorage interface [Windows Shell]","GetPropertyStorage method","IPersistSerializedPropStorage.GetPropertyStorage","IPersistSerializedPropStorage::GetPropertyStorage","_shell_IPersistSerializedPropStorage_GetPropertyStorage","propsys/IPersistSerializedPropStorage::GetPropertyStorage","shell.IPersistSerializedPropStorage_GetPropertyStorage"]
old-location: shell\IPersistSerializedPropStorage_GetPropertyStorage.htm
tech.root: shell
ms.assetid: 86a1d7ec-759a-4b8a-91e1-4cfa28a17b41
ms.date: 12/05/2018
ms.keywords: GetPropertyStorage, GetPropertyStorage method [Windows Shell], GetPropertyStorage method [Windows Shell],IPersistSerializedPropStorage interface, IPersistSerializedPropStorage interface [Windows Shell],GetPropertyStorage method, IPersistSerializedPropStorage.GetPropertyStorage, IPersistSerializedPropStorage::GetPropertyStorage, _shell_IPersistSerializedPropStorage_GetPropertyStorage, propsys/IPersistSerializedPropStorage::GetPropertyStorage, shell.IPersistSerializedPropStorage_GetPropertyStorage
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
 - IPersistSerializedPropStorage::GetPropertyStorage
 - propsys/IPersistSerializedPropStorage::GetPropertyStorage
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
 - IPersistSerializedPropStorage.GetPropertyStorage
---

# IPersistSerializedPropStorage::GetPropertyStorage


## -description

Gets the serialized property storage data from the property store instance.

## -parameters

### -param ppsps [out]

Type: <b>SERIALIZEDPROPSTORAGE**</b>

When this method returns, contains the address of a pointer to the serialized property storage data.

### -param pcb [out]

Type: <b>DWORD*</b>

When this method returns, contains the count of bytes contained in the serialized property storage data pointed to by <i>ppsps</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>SERIALIZEDPROPSTORAGE</b> type is defined in Propsys.h as an incomplete type. It should be treated as an array of <b>BYTE</b> values; the format of the returned data is not specified. The contents of the <b>SERIALIZEDPROPSTORAGE</b> structure are suitable for persisting to disk or other storage and can be used to initialize another property store through <a href="/windows/desktop/api/propsys/nf-propsys-ipersistserializedpropstorage-setpropertystorage">IPersistSerializedPropStorage::SetPropertyStorage</a>.

<div class="alert"><b>Note</b>  It is the responsibility of the application that calls <b>IPersistSerializedPropStorage::GetPropertyStorage</b> to later call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the memory referred to by <i>ppsps</i> when it is no longer needed.</div>
<div> </div>