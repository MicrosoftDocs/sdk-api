---
UID: NE:d3d10.D3D10_ASYNC_GETDATA_FLAG
title: D3D10_ASYNC_GETDATA_FLAG (d3d10.h)
description: Optional flags that control the behavior of ID3D10Asynchronous::GetData.
helpviewer_keywords: ["D3D10_ASYNC_GETDATA_DONOTFLUSH","D3D10_ASYNC_GETDATA_FLAG","D3D10_ASYNC_GETDATA_FLAG enumeration [Direct3D 10]","d0797ad1-e1be-88a9-fb81-7dba0cb6c9ea","d3d10/D3D10_ASYNC_GETDATA_DONOTFLUSH","d3d10/D3D10_ASYNC_GETDATA_FLAG","direct3d10.d3d10_async_getdata_flag"]
old-location: direct3d10\d3d10_async_getdata_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_async_getdata_flag.htm
ms.date: 12/05/2018
ms.keywords: D3D10_ASYNC_GETDATA_DONOTFLUSH, D3D10_ASYNC_GETDATA_FLAG, D3D10_ASYNC_GETDATA_FLAG enumeration [Direct3D 10], d0797ad1-e1be-88a9-fb81-7dba0cb6c9ea, d3d10/D3D10_ASYNC_GETDATA_DONOTFLUSH, d3d10/D3D10_ASYNC_GETDATA_FLAG, direct3d10.d3d10_async_getdata_flag
req.header: d3d10.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_ASYNC_GETDATA_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_ASYNC_GETDATA_FLAG
 - d3d10/D3D10_ASYNC_GETDATA_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_ASYNC_GETDATA_FLAG
---

# D3D10_ASYNC_GETDATA_FLAG enumeration


## -description

Optional flags that control the behavior of <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a>.

## -enum-fields

### -field D3D10_ASYNC_GETDATA_DONOTFLUSH:0x1

Do not flush the command buffer. This can potentially cause an infinite loop if GetData is continually called until it returns S_OK as there may still be commands in the command buffer that need to be processed in order for GetData to return S_OK. Since the commands in the command buffer are not flushed they will not be processed and therefore GetData will never return S_OK.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
