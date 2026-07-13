---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.Query
title: IDirect3DAuthenticatedChannel9::Query (d3d9.h)
description: Sends a query to the authenticated channel.
helpviewer_keywords: ["IDirect3DAuthenticatedChannel9 interface [Media Foundation]","Query method","IDirect3DAuthenticatedChannel9.Query","IDirect3DAuthenticatedChannel9::Query","Query","Query method [Media Foundation]","Query method [Media Foundation]","IDirect3DAuthenticatedChannel9 interface","d3d9/IDirect3DAuthenticatedChannel9::Query","mf.idirect3dauthenticatedchannel9_query"]
old-location: mf\idirect3dauthenticatedchannel9_query.htm
tech.root: mf
ms.assetid: 370ed31d-5b75-4767-b8d8-33cb2ff49fee
ms.date: 12/05/2018
ms.keywords: IDirect3DAuthenticatedChannel9 interface [Media Foundation],Query method, IDirect3DAuthenticatedChannel9.Query, IDirect3DAuthenticatedChannel9::Query, Query, Query method [Media Foundation], Query method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, d3d9/IDirect3DAuthenticatedChannel9::Query, mf.idirect3dauthenticatedchannel9_query
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IDirect3DAuthenticatedChannel9::Query
 - d3d9/IDirect3DAuthenticatedChannel9::Query
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DAuthenticatedChannel9.Query
---

# IDirect3DAuthenticatedChannel9::Query


## -description

Sends a query to the authenticated channel.

## -parameters

### -param InputSize

The size of the <i>pInput</i> array, in bytes.

### -param pInput

A pointer to a byte array that contains input data for the query. This array always starts with a <a href="/windows/desktop/medfound/d3dauthenticatedchannel-query-input">D3DAUTHENTICATEDCHANNEL_QUERY_INPUT</a> structure. The <b>QueryType</b> member of the structure specifies the query and defines the meaning of the rest of the array.

### -param OutputSize

The size of the <i>pOutput</i> array, in bytes.

### -param pOutput

A pointer to a byte array that receives the result of the query. This array always starts with a <a href="/windows/desktop/medfound/d3dauthenticatedchannel-query-output">D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT</a> structure. The meaning of the rest of the array depends on the query.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For a list of queries, see <a href="/windows/desktop/medfound/content-protection-queries">Content Protection Queries</a>.

## -see-also

<a href="/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>