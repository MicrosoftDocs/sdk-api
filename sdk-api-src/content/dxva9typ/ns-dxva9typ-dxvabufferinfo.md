---
UID: NS:dxva9typ._DXVABufferInfo
title: DXVABufferInfo (dxva9typ.h)
description: Specifies a buffer for the IDirect3DDXVADevice9::Execute method.
helpviewer_keywords: ["DXVABufferInfo","DXVABufferInfo structure [Media Foundation]","_DXVABufferInfo","dxva9typ/DXVABufferInfo","mf.dxvabufferinfo"]
old-location: mf\dxvabufferinfo.htm
tech.root: mf
ms.assetid: 048a3fcf-6076-4500-b5cc-edfe782f467b
ms.date: 12/05/2018
ms.keywords: DXVABufferInfo, DXVABufferInfo structure [Media Foundation], _DXVABufferInfo, dxva9typ/DXVABufferInfo, mf.dxvabufferinfo
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVABufferInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVABufferInfo
 - dxva9typ/_DXVABufferInfo
 - DXVABufferInfo
 - dxva9typ/DXVABufferInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVABufferInfo
---

# DXVABufferInfo structure


## -description

Specifies a buffer for the 
        <a href="/windows/desktop/medfound/idirect3ddxvadevice9-execute">IDirect3DDXVADevice9::Execute</a>  method.

## -struct-fields

### -field pCompSurface

A pointer to the <b>IDirect3DSurface9</b> interface.

### -field DataOffset

The offset of the relevant data from the beginning of the buffer, in bytes.

### -field DataSize

The size of the relevant data in the buffer, in bytes.

## -see-also

<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/idirect3ddxvadevice9">IDirect3DDXVADevice9</a>