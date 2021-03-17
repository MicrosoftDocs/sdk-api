---
UID: NF:d3d11_3.ID3D11DeviceContext3.Flush1
title: ID3D11DeviceContext3::Flush1 (d3d11_3.h)
description: Sends queued-up commands in the command buffer to the graphics processing unit (GPU), with a specified context type and an optional event handle to create an event query.
helpviewer_keywords: ["Flush1","Flush1 method [Direct3D 11]","Flush1 method [Direct3D 11]","ID3D11DeviceContext3 interface","ID3D11DeviceContext3 interface [Direct3D 11]","Flush1 method","ID3D11DeviceContext3.Flush1","ID3D11DeviceContext3::Flush1","d3d11_3/ID3D11DeviceContext3::Flush1","direct3d11.id3d11devicecontext3_flush1"]
old-location: direct3d11\id3d11devicecontext3_flush1.htm
tech.root: direct3d11
ms.assetid: DBDA19C3-EC4E-4C12-B1ED-A92E5CE28CED
ms.date: 12/05/2018
ms.keywords: Flush1, Flush1 method [Direct3D 11], Flush1 method [Direct3D 11],ID3D11DeviceContext3 interface, ID3D11DeviceContext3 interface [Direct3D 11],Flush1 method, ID3D11DeviceContext3.Flush1, ID3D11DeviceContext3::Flush1, d3d11_3/ID3D11DeviceContext3::Flush1, direct3d11.id3d11devicecontext3_flush1
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext3::Flush1
 - d3d11_3/ID3D11DeviceContext3::Flush1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext3.Flush1
---

# ID3D11DeviceContext3::Flush1


## -description

Sends queued-up commands in the command buffer to the graphics processing unit (GPU), with a specified context type and an optional event handle to create an event query.

## -parameters

### -param ContextType

Type: <b><a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_context_type">D3D11_CONTEXT_TYPE</a></b>

A <a href="/windows/desktop/api/d3d11_3/ne-d3d11_3-d3d11_context_type">D3D11_CONTEXT_TYPE</a> that specifies the context in which a query occurs, such as a 3D command queue, 3D compute queue, 3D copy queue, video, or image.

### -param hEvent [in, optional]

Type: <b>HANDLE</b>

An optional event handle. When specified, this method creates an event query.
            

<b>Flush1</b> operates asynchronously, therefore it can return either before or after the GPU finishes executing the queued graphics commands, which will eventually complete.
              To create an event query, you can call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createquery">ID3D11Device::CreateQuery</a> with the
              value <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_query">D3D11_QUERY_EVENT</a> value.
              To determine when the GPU is finished processing the graphics commands,
              you can then use that event query in a call to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a>.

## -remarks

<b>Flush1</b> has parameters.
          For more information, see
          <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>, which doesn't have parameters.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>