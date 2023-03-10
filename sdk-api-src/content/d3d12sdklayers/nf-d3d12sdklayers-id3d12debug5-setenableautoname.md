---
UID: NF:d3d12sdklayers.ID3D12Debug5.SetEnableAutoName
title: ID3D12Debug5::SetEnableAutoName
description: Configures the auto-naming of objects.
tech.root: direct3d12
ms.date: 07/26/2021
req.construct-type: function
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
f1_keywords:
 - ID3D12Debug5::SetEnableAutoName
 - d3d12sdklayers/ID3D12Debug5::SetEnableAutoName
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug5::SetEnableAutoName
---

## -description

Configures the auto-naming of objects.

## -parameters

### -param Enable

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

`true` to enable auto-naming; `false` to disable auto-naming.

## -remarks

By default, objects are not named unless you use [ID3D12Object::SetName](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setname) or [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) to assign a name.

It's a best practice to name all of your Direct3D 12 objects; at least in debug builds. Failing that, you might find it convenient to allow automatic name assignment in order to cover the gaps. Direct3D 12 objects created with auto-name enabled are automatically assigned a name, which is used for debug layer output and for DRED page fault data.

So as not to create a dependency on a specific auto-naming format, you can't retrieve the auto-name strings by using ID3D12Object::GetName or [ID3D12Object::GetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-getprivatedata). But, to generate a unique name string, Direct3D 12 uses the locally-unique identifier (LUID) assigned to every **ID3D12DeviceChild** object at create time. You can retrieve that LUID by using **ID3D12Object::GetPrivateData** with the **REFGUID** value *WKPDID_D3D12UniqueObjectId*. You might find that useful for your own object-naming schemas.

When debugging existing software, you can control auto-naming by using the *D3DConfig* graphics tools utility and the command `d3dconfig.exe device auto-debug-name=forced-on`.

Any object given a name using [ID3D12Object::SetName](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setname) or [ID3D12Object::SetPrivateData](/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedata) uses the assigned name instead of the auto-name.

## -see-also

* [ID3D12Debug5](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug5)
