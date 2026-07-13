---
UID: NN:relogger.ITraceRelogger
title: ITraceRelogger (relogger.h)
description: Provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.
helpviewer_keywords: ["ITraceRelogger","ITraceRelogger interface [ETW]","ITraceRelogger interface [ETW]","described","etw.itracerelogger","relogger/ITraceRelogger"]
old-location: etw\itracerelogger.htm
tech.root: ETW
ms.assetid: 08073b9a-5ae0-4e88-a502-647567418005
ms.date: 12/05/2018
ms.keywords: ITraceRelogger, ITraceRelogger interface [ETW], ITraceRelogger interface [ETW],described, etw.itracerelogger, relogger/ITraceRelogger
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
 - ITraceRelogger
 - relogger/ITraceRelogger
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
 - ITraceRelogger
---

# ITraceRelogger interface


## -description

The <b>ITraceRelogger</b>  interface provides access to the relogging functionality, allowing you to manipulate and relog events from an ETW trace stream.

## -inheritance

The <b>ITraceRelogger</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITraceRelogger</b> also has these types of members:

## -remarks

This interface is not supported on Windows 7 for the IA64 architecture.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>



<a href="/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>
