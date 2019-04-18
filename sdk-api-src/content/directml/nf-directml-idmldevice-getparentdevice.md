---
UID: NF:directml.IDMLDevice.GetParentDevice
title: IDMLDevice::GetParentDevice
author: windows-sdk-content
description: Retrieves the Direct3D 12 device that was used to create this DirectML device.
old-location: direct3d12\idmldevice_getparentdevice.htm
tech.root: direct3d12
ms.assetid: 1EE62E60-629A-4D3B-A8CD-C0D9D9FBCB93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetParentDevice, GetParentDevice method, GetParentDevice method,IDMLDevice interface, IDMLDevice interface,GetParentDevice method, IDMLDevice.GetParentDevice, IDMLDevice::GetParentDevice, direct3d12.idmldevice_getparentdevice, directml/IDMLDevice::GetParentDevice
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDevice.GetParentDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDevice::GetParentDevice


## -description






Retrieves the Direct3D 12 device that was used to create this DirectML device.


## -parameters




### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>.


### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the device. This is the address of a pointer to an <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>, representing  the device.


## -returns



Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.




## -see-also




[IDMLDevice](/windows/desktop/api/directml/nn-directml-idmldevice)
 

 

