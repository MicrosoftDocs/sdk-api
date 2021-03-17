---
UID: NF:swdevice.SwMemFree
title: SwMemFree function (swdevice.h)
description: Frees memory that other Software Device API functions allocated.
helpviewer_keywords: ["SwMemFree","SwMemFree function","swdevice.swmemfree","swdevice/SwMemFree"]
old-location: swdevice\swmemfree.htm
tech.root: swdevice
ms.assetid: DBA39124-D93A-4865-B4CB-B2FA66FBD417
ms.date: 12/05/2018
ms.keywords: SwMemFree, SwMemFree function, swdevice.swmemfree, swdevice/SwMemFree
req.header: swdevice.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Swdevice.lib; OneCoreUAP.lib on Windows 10
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SwMemFree
 - swdevice/SwMemFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - API-MS-Win-devices-swdevice-l1-1-0.dll
 - API-MS-Win-devices-swdevice-l1-1-1.dll
api_name:
 - SwMemFree
---

# SwMemFree function


## -description

Frees memory that other Software Device API functions allocated.

## -parameters

### -param pMem [in]

A pointer to the block of memory to free.

## -see-also

<a href="/windows/desktop/api/swdevice/nf-swdevice-swdeviceinterfaceregister">SwDeviceInterfaceRegister</a>