---
UID: NF:filehc.GetFileSizeFromContext
title: GetFileSizeFromContext function (filehc.h)
description: Reports the file size cached with the handle.
helpviewer_keywords: ["GetFileSizeFromContext","GetFileSizeFromContext function [Windows API]","filehc/GetFileSizeFromContext","winprog._getfilesizefromcontext"]
old-location: winprog\_getfilesizefromcontext.htm
tech.root: winprog
ms.assetid: c44aab72-d5c8-43e0-b2ec-032904806227
ms.date: 12/05/2018
ms.keywords: GetFileSizeFromContext, GetFileSizeFromContext function [Windows API], filehc/GetFileSizeFromContext, winprog._getfilesizefromcontext
req.header: filehc.h
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFileSizeFromContext
 - filehc/GetFileSizeFromContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - GetFileSizeFromContext
---

# GetFileSizeFromContext function


## -description

Reports the file size cached with the handle.

## -parameters

### -param pContext [in]

A pointer to the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure that is associated with the file.

### -param pcbFileSizeHigh [out]

A pointer to the byte count of the file.

## -returns

Returns the size of the file in bytes.

## -see-also

<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>