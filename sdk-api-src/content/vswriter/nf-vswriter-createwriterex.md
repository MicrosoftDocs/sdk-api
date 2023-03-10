---
UID: NF:vswriter.CreateWriterEx
title: CreateWriterEx function (vswriter.h)
description: This function is reserved for system use. (CreateWriterEx)
helpviewer_keywords: ["CreateWriterEx","CreateWriterEx function","base.createwriterex","vswriter/CreateWriterEx"]
old-location: base\createwriterex.htm
tech.root: base
ms.assetid: 044dde5c-599f-495b-8d5c-7a37833bcb41
ms.date: 12/05/2018
ms.keywords: CreateWriterEx, CreateWriterEx function, base.createwriterex, vswriter/CreateWriterEx
req.header: vswriter.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateWriterEx
 - vswriter/CreateWriterEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vswriter.h
 - Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
 - VssAPI.dll
api_name:
 - CreateWriterEx
---

# CreateWriterEx function


## -description

This function is reserved for system use. Do not use this function directly. To create a VSS writer, extend the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> class. The <b>CVssWriterEx</b> base class implicitly calls <b>CreateWriterEx</b>.

## -parameters

### -param pWriter [in]

Reserved.

### -param pWriterImpl [out]

Reserved.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>
