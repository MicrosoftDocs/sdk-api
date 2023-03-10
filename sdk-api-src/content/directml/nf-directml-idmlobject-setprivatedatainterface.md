---
UID: NF:directml.IDMLObject.SetPrivateDataInterface
title: IDMLObject::SetPrivateDataInterface
description: Associates an IUnknown-derived interface with the DirectML device object, and associates that interface with an application-defined GUID.
helpviewer_keywords: ["IDMLObject interface","SetPrivateDataInterface method","IDMLObject.SetPrivateDataInterface","IDMLObject::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method","SetPrivateDataInterface method","IDMLObject interface","direct3d12.idmlobject_setprivatedatainterface","directml/IDMLObject::SetPrivateDataInterface"]
old-location: direct3d12\idmlobject_setprivatedatainterface.htm
tech.root: directml
ms.assetid: 18D36A5A-07C4-4926-8B31-BBB75EAEC6A9
ms.date: 12/5/2018
ms.keywords: IDMLObject interface,SetPrivateDataInterface method, IDMLObject.SetPrivateDataInterface, IDMLObject::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method, SetPrivateDataInterface method,IDMLObject interface, direct3d12.idmlobject_setprivatedatainterface, directml/IDMLObject::SetPrivateDataInterface
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
 - IDMLObject::SetPrivateDataInterface
 - directml/IDMLObject::SetPrivateDataInterface
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
 - IDMLObject.SetPrivateDataInterface
---

# IDMLObject::SetPrivateDataInterface


## -description

Associates an <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface with the DirectML device object, and associates that interface with an application-defined <b>GUID</b>. This method is thread-safe.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The <b>GUID</b> to associate with the interface.

### -param data [in, optional]

Type: <b>const <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface to be associated with the device object.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLObject](/windows/win32/api/directml/nn-directml-idmlobject)
