---
UID: NN:relogger.ITraceEventCallback
title: ITraceEventCallback (relogger.h)
description: Used by ETW to provide information to the relogger as the tracing process starts, ends, and logs events.
helpviewer_keywords: ["IEventCallback","IEventCallback interface [ETW]","IEventCallback interface [ETW]","described","ITraceEventCallback","etw.ieventcallback","relogger/ITraceEventCallback"]
old-location: etw\ieventcallback.htm
tech.root: ETW
ms.assetid: 70139402-86e6-43b4-9016-42854ef998fd
ms.date: 12/05/2018
ms.keywords: IEventCallback, IEventCallback interface [ETW], IEventCallback interface [ETW],described, ITraceEventCallback, etw.ieventcallback, relogger/ITraceEventCallback
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
 - ITraceEventCallback
 - relogger/ITraceEventCallback
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
 - IEventCallback
---

# ITraceEventCallback interface


## -description

The <b>ITraceEventCallback</b>  interface is used by ETW to provide information to the relogger as the tracing process starts, ends, and logs events.

## -inheritance

The <b>IEventCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITraceEventCallback</b> also has these types of members:

## -remarks

This interface is not supported on Windows 7 for the IA64 architecture.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>



<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>
