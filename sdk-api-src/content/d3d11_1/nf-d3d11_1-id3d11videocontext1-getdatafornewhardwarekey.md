---
UID: NF:d3d11_1.ID3D11VideoContext1.GetDataForNewHardwareKey
title: ID3D11VideoContext1::GetDataForNewHardwareKey (d3d11_1.h)
description: Allows the driver to return IHV specific information used when initializing the new hardware key.
helpviewer_keywords: ["GetDataForNewHardwareKey","GetDataForNewHardwareKey method [Media Foundation]","GetDataForNewHardwareKey method [Media Foundation]","ID3D11VideoContext1 interface","ID3D11VideoContext1 interface [Media Foundation]","GetDataForNewHardwareKey method","ID3D11VideoContext1.GetDataForNewHardwareKey","ID3D11VideoContext1::GetDataForNewHardwareKey","d3d11_1/ID3D11VideoContext1::GetDataForNewHardwareKey","mf.id3d11videocontext1_getdatafornewhardwarekey"]
old-location: mf\id3d11videocontext1_getdatafornewhardwarekey.htm
tech.root: mf
ms.assetid: 4C02F80C-CF7A-4E66-9172-D55A31986ACD
ms.date: 12/05/2018
ms.keywords: GetDataForNewHardwareKey, GetDataForNewHardwareKey method [Media Foundation], GetDataForNewHardwareKey method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],GetDataForNewHardwareKey method, ID3D11VideoContext1.GetDataForNewHardwareKey, ID3D11VideoContext1::GetDataForNewHardwareKey, d3d11_1/ID3D11VideoContext1::GetDataForNewHardwareKey, mf.id3d11videocontext1_getdatafornewhardwarekey
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11VideoContext1::GetDataForNewHardwareKey
 - d3d11_1/ID3D11VideoContext1::GetDataForNewHardwareKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.GetDataForNewHardwareKey
---

# ID3D11VideoContext1::GetDataForNewHardwareKey


## -description

Allows the driver to return IHV specific information used when initializing the new hardware key.

## -parameters

### -param pCryptoSession [in]

Type: <b>ID3D11CryptoSession*</b>

A pointer to the ID3D11CryptoSession interface.  To get this pointer, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession">ID3D11VideoDevice1::CreateCryptoSession</a>.

### -param PrivateInputSize [in]

Type: <b>UINT</b>

The size of the memory referenced by the <i>pPrivateInputData</i> parameter.

### -param pPrivatInputData [in]

Type: <b>const void*</b>

The private input data. The contents of this parameter is defined by the implementation of the secure execution environment. It may contain data about the license or about the stream properties.

### -param pPrivateOutputData [out]

Type: <b>UINT64*</b>

A pointer to the private output data. The return data is defined by the implementation of the secure execution environment. It may contain graphics-specific data to be associated with the underlying hardware key.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>