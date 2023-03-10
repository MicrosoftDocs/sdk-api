---
UID: NF:directml.IDMLDevice.Evict
title: IDMLDevice::Evict
description: Evicts one or more pageable objects from GPU memory. Also see IDMLDevice::MakeResident.
helpviewer_keywords: ["Evict","Evict method","Evict method","IDMLDevice interface","IDMLDevice interface","Evict method","IDMLDevice.Evict","IDMLDevice::Evict","direct3d12.idmldevice_evict","directml/IDMLDevice::Evict"]
old-location: direct3d12\idmldevice_evict.htm
tech.root: directml
ms.assetid: 45FF300A-A645-4A1D-B2E1-924CD0E32F2B
ms.date: 12/5/2018
ms.keywords: Evict, Evict method, Evict method,IDMLDevice interface, IDMLDevice interface,Evict method, IDMLDevice.Evict, IDMLDevice::Evict, direct3d12.idmldevice_evict, directml/IDMLDevice::Evict
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
 - IDMLDevice::Evict
 - directml/IDMLDevice::Evict
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
 - IDMLDevice.Evict
---

# IDMLDevice::Evict


## -description

Evicts one or more pageable objects from GPU memory. Also see [IDMLDevice::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident).

## -parameters

### -param count

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This parameter determines the number of elements in the array passed in the  <i>ppObjects</i> parameter.

### -param ppObjects [in]

Type: <b>[IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable)*</b>

A pointer to a constant array of [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) pointers containing the pageable objects to evict from GPU memory.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)

[IDMLDevice::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident)
