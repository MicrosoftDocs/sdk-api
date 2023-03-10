---
UID: NF:directml.IDMLDevice.MakeResident
title: IDMLDevice::MakeResident
description: Causes one or more pageable objects to become resident in GPU memory. Also see IDMLDevice::Evict.
helpviewer_keywords: ["IDMLDevice interface","MakeResident method","IDMLDevice.MakeResident","IDMLDevice::MakeResident","MakeResident","MakeResident method","MakeResident method","IDMLDevice interface","direct3d12.idmldevice_makeresident","directml/IDMLDevice::MakeResident"]
old-location: direct3d12\idmldevice_makeresident.htm
tech.root: directml
ms.assetid: 966B23A1-5CE3-43C3-8D3B-2243C2D6322D
ms.date: 12/5/2018
ms.keywords: IDMLDevice interface,MakeResident method, IDMLDevice.MakeResident, IDMLDevice::MakeResident, MakeResident, MakeResident method, MakeResident method,IDMLDevice interface, direct3d12.idmldevice_makeresident, directml/IDMLDevice::MakeResident
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
 - IDMLDevice::MakeResident
 - directml/IDMLDevice::MakeResident
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
 - IDMLDevice.MakeResident
---

# IDMLDevice::MakeResident


## -description

Causes one or more pageable objects to become resident in GPU memory. Also see [IDMLDevice::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict).

## -parameters

### -param count

Type: <b>UINT</b>

This parameter determines the number of elements in the array passed in the  <i>ppObjects</i> parameter.

### -param ppObjects [in]

Type: <b>[IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable)*</b>

A pointer to a constant array of [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) pointers containing the pageable objects to make resident in GPU memory.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)

[IDMLDevice::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict)
