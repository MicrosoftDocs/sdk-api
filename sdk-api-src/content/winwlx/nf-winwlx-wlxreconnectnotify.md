---
UID: NF:winwlx.WlxReconnectNotify
title: WlxReconnectNotify
ms.date: 11/4/2019
targetos: Windows
description: Winlogon calls this function when a Terminal Services network session is reconnected.
helpviewer_keywords: ["WlxReconnectNotify"]
tech.root: security
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winwlx.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - msgina.dll
api_name:
 - WlxReconnectNotify
f1_keywords:
 - WlxReconnectNotify
 - winwlx/WlxReconnectNotify
dev_langs:
 - c++
---

## -description

Winlogon calls this function when a Terminal Services network session is reconnected.

## -parameters

### -param pWlxContext

A pointer to the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> context associated with this window station.

## -remarks

## -see-also
