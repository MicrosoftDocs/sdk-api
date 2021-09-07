---
UID: NF:relogger.ITraceRelogger.SetOutputFilename
title: ITraceRelogger::SetOutputFilename (relogger.h)
description: Indicates the file to which ETW should write the new, relogged trace.
helpviewer_keywords: ["ITraceRelogger interface [ETW]","SetOutputFilename method","ITraceRelogger.SetOutputFilename","ITraceRelogger::SetOutputFilename","SetOutputFilename","SetOutputFilename method [ETW]","SetOutputFilename method [ETW]","ITraceRelogger interface","etw.itracerelogger_setoutputfilename","relogger/ITraceRelogger::SetOutputFilename"]
old-location: etw\itracerelogger_setoutputfilename.htm
tech.root: ETW
ms.assetid: ed3f8bcd-88c7-4d05-a396-41ee8f35bc97
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],SetOutputFilename method, ITraceRelogger.SetOutputFilename, ITraceRelogger::SetOutputFilename, SetOutputFilename, SetOutputFilename method [ETW], SetOutputFilename method [ETW],ITraceRelogger interface, etw.itracerelogger_setoutputfilename, relogger/ITraceRelogger::SetOutputFilename
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
 - ITraceRelogger::SetOutputFilename
 - relogger/ITraceRelogger::SetOutputFilename
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
 - ITraceRelogger.SetOutputFilename
---

# ITraceRelogger::SetOutputFilename


## -description

The <b>SetOutputFilename</b> method indicates the file to which ETW should write the new, relogged trace.

## -parameters

### -param LogfileName [in]

Type: <b>BSTR</b>

The new filename.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the indicated file already exists, it will be overwritten with the new trace.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>