---
UID: NF:propsys.IPersistSerializedPropStorage2.GetPropertyStorageSize
title: IPersistSerializedPropStorage2::GetPropertyStorageSize (propsys.h)
description: Gets the size of serialized property storage data from the property store instance.
helpviewer_keywords: ["GetPropertyStorageSize","GetPropertyStorageSize method [Windows Shell]","GetPropertyStorageSize method [Windows Shell]","IPersistSerializedPropStorage2 interface","IPersistSerializedPropStorage2 interface [Windows Shell]","GetPropertyStorageSize method","IPersistSerializedPropStorage2.GetPropertyStorageSize","IPersistSerializedPropStorage2::GetPropertyStorageSize","_shell_IPersistSerializedPropStorage2_GetPropertyStorageSize","propsys/IPersistSerializedPropStorage2::GetPropertyStorageSize","shell.IPersistSerializedPropStorage2_GetPropertyStorageSize"]
old-location: shell\IPersistSerializedPropStorage2_GetPropertyStorageSize.htm
tech.root: shell
ms.assetid: 90fe3148-457e-4d29-a117-b0b0e0df92c4
ms.date: 12/05/2018
ms.keywords: GetPropertyStorageSize, GetPropertyStorageSize method [Windows Shell], GetPropertyStorageSize method [Windows Shell],IPersistSerializedPropStorage2 interface, IPersistSerializedPropStorage2 interface [Windows Shell],GetPropertyStorageSize method, IPersistSerializedPropStorage2.GetPropertyStorageSize, IPersistSerializedPropStorage2::GetPropertyStorageSize, _shell_IPersistSerializedPropStorage2_GetPropertyStorageSize, propsys/IPersistSerializedPropStorage2::GetPropertyStorageSize, shell.IPersistSerializedPropStorage2_GetPropertyStorageSize
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPersistSerializedPropStorage2::GetPropertyStorageSize
 - propsys/IPersistSerializedPropStorage2::GetPropertyStorageSize
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
 - IPersistSerializedPropStorage2.GetPropertyStorageSize
---

# IPersistSerializedPropStorage2::GetPropertyStorageSize


## -description

Gets the size of serialized property storage data from the property store instance.

## -parameters

### -param pcb [out]

Type: <b>DWORD*</b>

The count of bytes contained in the serialized property storage data.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

