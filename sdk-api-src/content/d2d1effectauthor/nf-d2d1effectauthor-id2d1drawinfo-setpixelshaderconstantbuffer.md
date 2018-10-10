---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetPixelShaderConstantBuffer
title: ID2D1DrawInfo::SetPixelShaderConstantBuffer
author: windows-sdk-content
description: Sets the constant buffer for this transform's pixel shader.
old-location: direct2d\id2d1drawinfo_setpixelshaderconstantbuffer.htm
tech.root: Direct2D
ms.assetid: 3A32E831-3754-4EF5-B559-ED02EF747897
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetPixelShaderConstantBuffer method, ID2D1DrawInfo.SetPixelShaderConstantBuffer, ID2D1DrawInfo::SetPixelShaderConstantBuffer, SetPixelShaderConstantBuffer, SetPixelShaderConstantBuffer method [Direct2D], SetPixelShaderConstantBuffer method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetPixelShaderConstantBuffer, direct2d.id2d1drawinfo_setpixelshaderconstantbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetPixelShaderConstantBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo::SetPixelShaderConstantBuffer


## -description


Sets the constant buffer for this transform's pixel shader.


## -parameters




### -param buffer [in]

Type: <b>const BYTE*</b>

The data applied to the constant buffer.


### -param bufferCount

Type: <b>UINT32</b>

The number of bytes of data in the constant buffer


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253">ID2D1DrawInfo</a>
 

 

