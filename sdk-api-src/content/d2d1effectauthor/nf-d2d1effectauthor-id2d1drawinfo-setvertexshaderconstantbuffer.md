---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetVertexShaderConstantBuffer
title: ID2D1DrawInfo::SetVertexShaderConstantBuffer
author: windows-sdk-content
description: Sets the constant buffer for this transform's vertex shader.
old-location: direct2d\id2d1drawinfo_setvertexshaderconstantbuffer.htm
tech.root: direct2d
ms.assetid: 1A7991C9-BB3F-4E58-9FA7-5C4B194C33F6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetVertexShaderConstantBuffer method, ID2D1DrawInfo.SetVertexShaderConstantBuffer, ID2D1DrawInfo::SetVertexShaderConstantBuffer, SetVertexShaderConstantBuffer, SetVertexShaderConstantBuffer method [Direct2D], SetVertexShaderConstantBuffer method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetVertexShaderConstantBuffer, direct2d.id2d1drawinfo_setvertexshaderconstantbuffer
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
 - ID2D1DrawInfo.SetVertexShaderConstantBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo::SetVertexShaderConstantBuffer


## -description


Sets the constant buffer for this transform's vertex shader.


## -parameters




### -param buffer [in]

Type: <b>const BYTE*</b>

The data applied to the constant buffer


### -param bufferCount

Type: <b>UINT32</b>

The number of bytes of data in the constant buffer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253">ID2D1DrawInfo</a>
 

 

