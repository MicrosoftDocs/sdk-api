---
UID: NF:relogger.ITraceRelogger.SetCompressionMode
title: ITraceRelogger::SetCompressionMode (relogger.h)
description: Enables or disables compression on the relogged trace.
helpviewer_keywords: ["ITraceRelogger interface [ETW]","SetCompressionMode method","ITraceRelogger.SetCompressionMode","ITraceRelogger::SetCompressionMode","SetCompressionMode","SetCompressionMode method [ETW]","SetCompressionMode method [ETW]","ITraceRelogger interface","etw.itracerelogger_setcompressionmode","relogger/ITraceRelogger::SetCompressionMode"]
old-location: etw\itracerelogger_setcompressionmode.htm
tech.root: ETW
ms.assetid: 2a758af0-2316-4c4b-8717-ee1ebad205ee
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],SetCompressionMode method, ITraceRelogger.SetCompressionMode, ITraceRelogger::SetCompressionMode, SetCompressionMode, SetCompressionMode method [ETW], SetCompressionMode method [ETW],ITraceRelogger interface, etw.itracerelogger_setcompressionmode, relogger/ITraceRelogger::SetCompressionMode
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
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
 - ITraceRelogger::SetCompressionMode
 - relogger/ITraceRelogger::SetCompressionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceRelogger.SetCompressionMode
---

# ITraceRelogger::SetCompressionMode


## -description

The <b>SetCompressionMode</b> method enables or disables compression on the relogged trace.

## -parameters

### -param CompressionMode [in]

Type: <b>BOOLEAN</b>

True if compression is enabled; otherwise, false.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

By default, compression will be enabled on a relogged trace.

Compression mode is not supported on Windows 7. By default,  Compression mode it is set to <b>false</b> on Windows 7. When this method is called,   it returns <b>E_NOTIMPL</b> when called on Windows 7.


Compression mode is set  to <b>true</b> on Windows 8 or Windows Server 2012.

Compressed trace files can only be decoded in Windows 8 or Windows Server 2012.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>