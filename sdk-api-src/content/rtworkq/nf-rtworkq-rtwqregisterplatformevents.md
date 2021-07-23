---
UID: NF:rtworkq.RtwqRegisterPlatformEvents
title: RtwqRegisterPlatformEvents function (rtworkq.h)
description: Enables an app to listen to the RtwqStartup and RtwqShutdown functions.
helpviewer_keywords: ["RtwqRegisterPlatformEvents","RtwqRegisterPlatformEvents function","base.rtwqregisterplatformevents","rtworkq/RtwqRegisterPlatformEvents"]
old-location: base\rtwqregisterplatformevents.htm
tech.root: backup
ms.assetid: 7BD7E83B-29E1-4FF5-B527-71C2F80D6521
ms.date: 12/05/2018
ms.keywords: RtwqRegisterPlatformEvents, RtwqRegisterPlatformEvents function, base.rtwqregisterplatformevents, rtworkq/RtwqRegisterPlatformEvents
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
 - RtwqRegisterPlatformEvents
 - rtworkq/RtwqRegisterPlatformEvents
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
 - RtwqRegisterPlatformEvents
---

# RtwqRegisterPlatformEvents function


## -description

Enables an app to listen to the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqstartup">RtwqStartup</a> and <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqshutdown">RtwqShutdown</a> functions.

## -parameters

### -param platformEvents [in]

Pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqplatformevents">IRtwqPlatformEvents</a> object which provides the events.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.