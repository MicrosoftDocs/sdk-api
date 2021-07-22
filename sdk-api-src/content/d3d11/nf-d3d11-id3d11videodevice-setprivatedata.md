---
UID: NF:d3d11.ID3D11VideoDevice.SetPrivateData
title: ID3D11VideoDevice::SetPrivateData (d3d11.h)
description: Sets private data on the video device and associates that data with a GUID.
helpviewer_keywords: ["ID3D11VideoDevice interface [Media Foundation]","SetPrivateData method","ID3D11VideoDevice.SetPrivateData","ID3D11VideoDevice::SetPrivateData","SetPrivateData","SetPrivateData method [Media Foundation]","SetPrivateData method [Media Foundation]","ID3D11VideoDevice interface","d3d11/ID3D11VideoDevice::SetPrivateData","mf.id3d11videodevice_setprivatedata"]
old-location: mf\id3d11videodevice_setprivatedata.htm
tech.root: mf
ms.assetid: B7B9E225-A27E-4278-B191-08C0C93C86AC
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice interface [Media Foundation],SetPrivateData method, ID3D11VideoDevice.SetPrivateData, ID3D11VideoDevice::SetPrivateData, SetPrivateData, SetPrivateData method [Media Foundation], SetPrivateData method [Media Foundation],ID3D11VideoDevice interface, d3d11/ID3D11VideoDevice::SetPrivateData, mf.id3d11videodevice_setprivatedata
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
 - ID3D11VideoDevice::SetPrivateData
 - d3d11/ID3D11VideoDevice::SetPrivateData
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
 - ID3D11VideoDevice.SetPrivateData
---

# ID3D11VideoDevice::SetPrivateData


## -description

Sets private data on the video device and associates that data with a GUID.

## -parameters

### -param guid [in]

The GUID associated with the data.

### -param DataSize [in]

The size of the data, in bytes.

### -param pData [in]

A pointer to the data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>