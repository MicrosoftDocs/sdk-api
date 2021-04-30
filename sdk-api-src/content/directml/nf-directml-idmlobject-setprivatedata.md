---
UID: NF:directml.IDMLObject.SetPrivateData
title: IDMLObject::SetPrivateData
description: Sets application-defined data to a DirectML device object, and associates that data with an application-defined GUID.
helpviewer_keywords: ["IDMLObject interface","SetPrivateData method","IDMLObject.SetPrivateData","IDMLObject::SetPrivateData","SetPrivateData","SetPrivateData method","SetPrivateData method","IDMLObject interface","direct3d12.idmlobject_setprivatedata","directml/IDMLObject::SetPrivateData"]
old-location: direct3d12\idmlobject_setprivatedata.htm
tech.root: directml
ms.assetid: 9409CC38-63E8-4A44-9746-A075E664A4E9
ms.date: 12/5/2018
ms.keywords: IDMLObject interface,SetPrivateData method, IDMLObject.SetPrivateData, IDMLObject::SetPrivateData, SetPrivateData, SetPrivateData method, SetPrivateData method,IDMLObject interface, direct3d12.idmlobject_setprivatedata, directml/IDMLObject::SetPrivateData
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLObject::SetPrivateData
 - directml/IDMLObject::SetPrivateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLObject.SetPrivateData
---

# IDMLObject::SetPrivateData


## -description

Sets application-defined data to a DirectML device object, and associates that data with an application-defined <b>GUID</b>. This method is thread-safe.

## -parameters

### -param guid

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The <b>GUID</b> to associate with the data.

### -param dataSize [in]

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size in bytes of the data.

### -param data [in, optional]

Type: <b>const void*</b>

A pointer to a memory block that contains the data to be stored with this DirectML device object. If <i>data</i> is <b>NULL</b>, then <i>dataSize</i> must be 0, and any data that was previously associated with the <b>GUID</b> specified in <i>guid</i> will be destroyed.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLObject](/windows/win32/api/directml/nn-directml-idmlobject)
