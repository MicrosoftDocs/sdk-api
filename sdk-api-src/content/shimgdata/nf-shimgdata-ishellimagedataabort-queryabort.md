---
UID: NF:shimgdata.IShellImageDataAbort.QueryAbort
title: IShellImageDataAbort::QueryAbort (shimgdata.h)
description: Aborts an IShellImageData process such as Decode, Draw, or Scale. This is a callback method.
helpviewer_keywords: ["IShellImageDataAbort interface [Windows Shell]","QueryAbort method","IShellImageDataAbort.QueryAbort","IShellImageDataAbort::QueryAbort","QueryAbort","QueryAbort method [Windows Shell]","QueryAbort method [Windows Shell]","IShellImageDataAbort interface","_shell_IShellImageDataAbort_QueryAbort","shell.IShellImageDataAbort_QueryAbort","shimgdata/IShellImageDataAbort::QueryAbort"]
old-location: shell\IShellImageDataAbort_QueryAbort.htm
tech.root: shell
ms.assetid: 88823fe3-efde-4ee1-9b4f-685f8df03b29
ms.date: 12/05/2018
ms.keywords: IShellImageDataAbort interface [Windows Shell],QueryAbort method, IShellImageDataAbort.QueryAbort, IShellImageDataAbort::QueryAbort, QueryAbort, QueryAbort method [Windows Shell], QueryAbort method [Windows Shell],IShellImageDataAbort interface, _shell_IShellImageDataAbort_QueryAbort, shell.IShellImageDataAbort_QueryAbort, shimgdata/IShellImageDataAbort::QueryAbort
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageDataAbort::QueryAbort
 - shimgdata/IShellImageDataAbort::QueryAbort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageDataAbort.QueryAbort
---

# IShellImageDataAbort::QueryAbort


## -description

Aborts an <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> process such as <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">Decode</a>, <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-draw">Draw</a>, or <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-scale">Scale</a>. This is a callback method.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> process should continue, or S_FALSE if it should be aborted.
