---
UID: NF:directml.IDMLObject.GetPrivateData
title: IDMLObject::GetPrivateData
description: Gets application-defined data from a DirectML device object.
helpviewer_keywords: ["GetPrivateData","GetPrivateData method","GetPrivateData method","IDMLObject interface","IDMLObject interface","GetPrivateData method","IDMLObject.GetPrivateData","IDMLObject::GetPrivateData","direct3d12.idmlobject_getprivatedata","directml/IDMLObject::GetPrivateData"]
old-location: direct3d12\idmlobject_getprivatedata.htm
tech.root: directml
ms.assetid: 9AB29A57-95F4-4DB4-9D67-A8354CD93B81
ms.date: 12/5/2018
ms.keywords: GetPrivateData, GetPrivateData method, GetPrivateData method,IDMLObject interface, IDMLObject interface,GetPrivateData method, IDMLObject.GetPrivateData, IDMLObject::GetPrivateData, direct3d12.idmlobject_getprivatedata, directml/IDMLObject::GetPrivateData
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
 - IDMLObject::GetPrivateData
 - directml/IDMLObject::GetPrivateData
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
 - IDMLObject.GetPrivateData
---

## -description

Gets application-defined data from a DirectML device object. This method is thread-safe.

## -parameters

### -param guid [in]

Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

The <b>GUID</b> that is associated with the data.

### -param dataSize [in, out]

Type: <b>[UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>data</i> points to, and on output contains the size, in bytes, of the amount of data that <b>GetPrivateData</b> retrieved.

### -param data [out, optional]

Type: <b>void*</b>

A pointer to a memory block that receives the data from the device object if <i>dataSize</i> points to a value that specifies a buffer large enough to hold the data.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

If the data returned is a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (or derived interface) that was previously set by [SetPrivateDataInterface](/windows/win32/api/directml/nf-directml-idmlobject-setprivatedatainterface), then that interface will have its reference count incremented before the private data is returned.

## -see-also

[IDMLObject](/windows/win32/api/directml/nn-directml-idmlobject)
