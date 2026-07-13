---
UID: NF:d3d11.ID3D11VideoDevice.SetPrivateDataInterface
title: ID3D11VideoDevice::SetPrivateDataInterface (d3d11.h)
description: Sets a private IUnknown pointer on the video device and associates that pointer with a GUID.
helpviewer_keywords: ["ID3D11VideoDevice interface [Media Foundation]","SetPrivateDataInterface method","ID3D11VideoDevice.SetPrivateDataInterface","ID3D11VideoDevice::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method [Media Foundation]","SetPrivateDataInterface method [Media Foundation]","ID3D11VideoDevice interface","d3d11/ID3D11VideoDevice::SetPrivateDataInterface","mf.id3d11videodevice_setprivatedatainterface"]
old-location: mf\id3d11videodevice_setprivatedatainterface.htm
tech.root: mf
ms.assetid: E20FC248-92B2-4284-9EDC-9D5E6AB9506B
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice interface [Media Foundation],SetPrivateDataInterface method, ID3D11VideoDevice.SetPrivateDataInterface, ID3D11VideoDevice::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Media Foundation], SetPrivateDataInterface method [Media Foundation],ID3D11VideoDevice interface, d3d11/ID3D11VideoDevice::SetPrivateDataInterface, mf.id3d11videodevice_setprivatedatainterface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoDevice::SetPrivateDataInterface
 - d3d11/ID3D11VideoDevice::SetPrivateDataInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.SetPrivateDataInterface
---

# ID3D11VideoDevice::SetPrivateDataInterface


## -description

Sets a private <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer on the video device and associates that pointer with a GUID.

## -parameters

### -param guid [in]

The GUID associated with the pointer.

### -param pData [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>