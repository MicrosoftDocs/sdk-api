---
UID: NF:directml.IDMLDeviceChild.GetDevice
title: IDMLDeviceChild::GetDevice
description: Retrieves the DirectML device that was used to create this object.
helpviewer_keywords: ["GetDevice","GetDevice method","GetDevice method","IDMLDeviceChild interface","IDMLDeviceChild interface","GetDevice method","IDMLDeviceChild.GetDevice","IDMLDeviceChild::GetDevice","direct3d12.idmldevicechild_getdevice","directml/IDMLDeviceChild::GetDevice"]
old-location: direct3d12\idmldevicechild_getdevice.htm
tech.root: directml
ms.assetid: 9839C889-D6F7-401A-A335-B2F63C8F30D8
ms.date: 12/5/2018
ms.keywords: GetDevice, GetDevice method, GetDevice method,IDMLDeviceChild interface, IDMLDeviceChild interface,GetDevice method, IDMLDeviceChild.GetDevice, IDMLDeviceChild::GetDevice, direct3d12.idmldevicechild_getdevice, directml/IDMLDeviceChild::GetDevice
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
 - IDMLDeviceChild::GetDevice
 - directml/IDMLDeviceChild::GetDevice
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
 - IDMLDeviceChild.GetDevice
---

# IDMLDeviceChild::GetDevice


## -description

Retrieves the DirectML device that was used to create this object.

## -parameters

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the DirectML device. This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild)
