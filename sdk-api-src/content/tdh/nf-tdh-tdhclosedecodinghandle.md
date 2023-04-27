---
UID: NF:tdh.TdhCloseDecodingHandle
title: TdhCloseDecodingHandle function (tdh.h)
description: Frees any resources associated with the input decoding handle.
helpviewer_keywords: ["TdhCloseDecodingHandle","TdhCloseDecodingHandle function [ETW]","etw.tdhclosedecodinghandle","tdh/TdhCloseDecodingHandle"]
old-location: etw\tdhclosedecodinghandle.htm
tech.root: ETW
ms.assetid: f3cf6b1e-c970-4b91-aa54-370d46a6e86a
ms.date: 12/05/2018
ms.keywords: TdhCloseDecodingHandle, TdhCloseDecodingHandle function [ETW], etw.tdhclosedecodinghandle, tdh/TdhCloseDecodingHandle
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhCloseDecodingHandle
 - tdh/TdhCloseDecodingHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhCloseDecodingHandle
---

# TdhCloseDecodingHandle function


## -description

Frees any resources associated with the input decoding handle.

## -parameters

### -param Handle [in]

Type: <b>TDH_HANDLE</b>

The decoding handle to be closed.

## -returns

Type: <b>ULONG</b>

This function returns ERROR_SUCCESS on completion.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhopendecodinghandle">TdhOpenDecodingHandle</a>