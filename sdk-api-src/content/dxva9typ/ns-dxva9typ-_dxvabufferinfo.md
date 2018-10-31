---
UID: NS:dxva9typ._DXVABufferInfo
title: "_DXVABufferInfo"
author: windows-sdk-content
description: Specifies a buffer for the IDirect3DDXVADevice9::Execute method.
old-location: mf\dxvabufferinfo.htm
tech.root: medfound
ms.assetid: 048a3fcf-6076-4500-b5cc-edfe782f467b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DXVABufferInfo, DXVABufferInfo structure [Media Foundation], _DXVABufferInfo, dxva9typ/DXVABufferInfo, mf.dxvabufferinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - DXVABufferInfo
product: Windows
targetos: Windows
req.typenames: DXVABufferInfo
req.redist: 
---

# _DXVABufferInfo structure


## -description


Specifies a buffer for the 
        <a href="https://msdn.microsoft.com/cb87a087-ca53-470e-ab46-f4022cfd7869">IDirect3DDXVADevice9::Execute</a>  method.


## -struct-fields




### -field pCompSurface

A pointer to the <b>IDirect3DSurface9</b> interface.


### -field DataOffset

The offset of the relevant data from the beginning of the buffer, in bytes.


### -field DataSize

The size of the relevant data in the buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 

