---
UID: NF:rtworkq.RtwqShutdown
title: RtwqShutdown function (rtworkq.h)
description: Shuts down the platform. Call this function once for every call to RtwqStartup. Do not call this function from work queue threads.
helpviewer_keywords: ["RtwqShutdown","RtwqShutdown function","base.rtwqshutdown","rtworkq/RtwqShutdown"]
old-location: base\rtwqshutdown.htm
tech.root: backup
ms.assetid: 806c4142-b628-4ea0-b5e2-d2b4ead73c04
ms.date: 12/05/2018
ms.keywords: RtwqShutdown, RtwqShutdown function, base.rtwqshutdown, rtworkq/RtwqShutdown
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqShutdown
 - rtworkq/RtwqShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqShutdown
---

# RtwqShutdown function


## -description

Shuts down the platform. Call this function once for every call to <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqstartup">RtwqStartup</a>. Do not call this function from work queue threads.



## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In general, apps should not have pending work after they call this function.
