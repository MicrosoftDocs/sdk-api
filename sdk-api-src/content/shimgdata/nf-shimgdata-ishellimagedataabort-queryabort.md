---
UID: NF:shimgdata.IShellImageDataAbort.QueryAbort
title: IShellImageDataAbort::QueryAbort (shimgdata.h)
description: Aborts an IShellImageData process such as Decode, Draw, or Scale. This is a callback method.
old-location: shell\IShellImageDataAbort_QueryAbort.htm
tech.root: shell
ms.assetid: 88823fe3-efde-4ee1-9b4f-685f8df03b29
ms.date: 12/05/2018
ms.keywords: IShellImageDataAbort interface [Windows Shell],QueryAbort method, IShellImageDataAbort.QueryAbort, IShellImageDataAbort::QueryAbort, QueryAbort, QueryAbort method [Windows Shell], QueryAbort method [Windows Shell],IShellImageDataAbort interface, _shell_IShellImageDataAbort_QueryAbort, shell.IShellImageDataAbort_QueryAbort, shimgdata/IShellImageDataAbort::QueryAbort
f1_keywords:
- shimgdata/IShellImageDataAbort.QueryAbort
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellImageDataAbort.QueryAbort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellImageDataAbort::QueryAbort


## -description


Aborts an <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> process such as <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">Decode</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-draw">Draw</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-scale">Scale</a>. This is a callback method.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> process should continue, or S_FALSE if it should be aborted.



