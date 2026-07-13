---
UID: NN:dwrite_3.IDWriteAsyncResult
title: IDWriteAsyncResult (dwrite_3.h)
description: Represents the result of an asynchronous operation. A client can use the interface to wait for the operation to complete and to get the result.
helpviewer_keywords: ["IDWriteAsyncResult","IDWriteAsyncResult interface [Direct Write]","IDWriteAsyncResult interface [Direct Write]","described","directwrite.idwriteasyncresult","dwrite_3/IDWriteAsyncResult"]
old-location: directwrite\idwriteasyncresult.htm
tech.root: DirectWrite
ms.assetid: 8F267213-EB98-4AD9-826A-7D4E34FEB3E4
ms.date: 09/10/2025
ms.keywords: IDWriteAsyncResult, IDWriteAsyncResult interface [Direct Write], IDWriteAsyncResult interface [Direct Write],described, directwrite.idwriteasyncresult, dwrite_3/IDWriteAsyncResult
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteAsyncResult
 - dwrite_3/IDWriteAsyncResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteAsyncResult
---

# IDWriteAsyncResult interface


## -description

Represents the result of an asynchronous
          operation. A client can use the interface to wait for the operation to
          complete and to get the result.

## -inheritance

The <b>IDWriteAsyncResult</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteAsyncResult</b> also has these types of members:

## -remarks

IDWriteAsyncResult is returned by <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-begindownload">IDWriteRemoteFontFileStream::BeginDownload</a> for signaling completion of a font download operation.

