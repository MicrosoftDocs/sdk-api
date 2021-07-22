---
UID: NF:rtworkq.RtwqUnregisterPlatformEvents
title: RtwqUnregisterPlatformEvents function (rtworkq.h)
description: Unregisters a listener event from the callback platform.
helpviewer_keywords: ["RtwqUnregisterPlatformEvents","RtwqUnregisterPlatformEvents function","base.rtwqunregisterplatformevents","rtworkq/RtwqUnregisterPlatformEvents"]
old-location: base\rtwqunregisterplatformevents.htm
tech.root: backup
ms.assetid: C1AB42C4-745B-46D6-9A1C-B5FD2443F48B
ms.date: 12/05/2018
ms.keywords: RtwqUnregisterPlatformEvents, RtwqUnregisterPlatformEvents function, base.rtwqunregisterplatformevents, rtworkq/RtwqUnregisterPlatformEvents
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
 - RtwqUnregisterPlatformEvents
 - rtworkq/RtwqUnregisterPlatformEvents
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
 - RtwqUnregisterPlatformEvents
---

# RtwqUnregisterPlatformEvents function


## -description

Unregisters a listener event from the callback platform.

## -parameters

### -param platformEvents

Pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqplatformevents">IRtwqPlatformEvents</a>  object which provides the events.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The app should use the same pointer that was passed to <a href="/windows/win32/api/rtworkq/nf-rtworkq-rtwqregisterplatformevents">RtwqRegisterPlatformEvents</a>.