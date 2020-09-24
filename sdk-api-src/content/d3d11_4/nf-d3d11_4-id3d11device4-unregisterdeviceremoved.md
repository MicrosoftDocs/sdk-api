---
UID: NF:d3d11_4.ID3D11Device4.UnregisterDeviceRemoved
title: ID3D11Device4::UnregisterDeviceRemoved (d3d11_4.h)
description: Unregisters the &quot;device removed&quot; event.
helpviewer_keywords: ["ID3D11Device4 interface [Direct3D 11]","UnregisterDeviceRemoved method","ID3D11Device4.UnregisterDeviceRemoved","ID3D11Device4::UnregisterDeviceRemoved","UnregisterDeviceRemoved","UnregisterDeviceRemoved method [Direct3D 11]","UnregisterDeviceRemoved method [Direct3D 11]","ID3D11Device4 interface","d3d11_4/ID3D11Device4::UnregisterDeviceRemoved","direct3d11.id3d11device4_unregisterdeviceremoved"]
old-location: direct3d11\id3d11device4_unregisterdeviceremoved.htm
tech.root: direct3d11
ms.assetid: F1B8BBD2-3D7D-4125-953F-D10D073B77AF
ms.date: 12/05/2018
ms.keywords: ID3D11Device4 interface [Direct3D 11],UnregisterDeviceRemoved method, ID3D11Device4.UnregisterDeviceRemoved, ID3D11Device4::UnregisterDeviceRemoved, UnregisterDeviceRemoved, UnregisterDeviceRemoved method [Direct3D 11], UnregisterDeviceRemoved method [Direct3D 11],ID3D11Device4 interface, d3d11_4/ID3D11Device4::UnregisterDeviceRemoved, direct3d11.id3d11device4_unregisterdeviceremoved
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device4::UnregisterDeviceRemoved
 - d3d11_4/ID3D11Device4::UnregisterDeviceRemoved
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device4.UnregisterDeviceRemoved
---

# ID3D11Device4::UnregisterDeviceRemoved


## -description

Unregisters the "device removed" event.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

Information about the "device removed" event,
          retrieved during a successful <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent">RegisterDeviceRemovedEvent</a> call.

## -remarks

See <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent">RegisterDeviceRemovedEvent</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4">ID3D11Device4</a>



<a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent">RegisterDeviceRemovedEvent</a>