---
UID: NF:wdstpdi.WdsTransportServerAllocateBuffer
title: WdsTransportServerAllocateBuffer function (wdstpdi.h)
description: Allocates a buffer in memory.
helpviewer_keywords: ["WdsTransportServerAllocateBuffer","WdsTransportServerAllocateBuffer function [Windows Deployment Services]","wds.wdstransportserverallocatebuffer","wdstpdi/WdsTransportServerAllocateBuffer"]
old-location: wds\wdstransportserverallocatebuffer.htm
tech.root: wds
ms.assetid: 0e227f46-a6f6-4fed-ac33-6e4e54f8b14d
ms.date: 12/05/2018
ms.keywords: WdsTransportServerAllocateBuffer, WdsTransportServerAllocateBuffer function [Windows Deployment Services], wds.wdstransportserverallocatebuffer, wdstpdi/WdsTransportServerAllocateBuffer
req.header: wdstpdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdsmc.lib
req.dll: Wdsmc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportServerAllocateBuffer
 - wdstpdi/WdsTransportServerAllocateBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsmc.dll
api_name:
 - WdsTransportServerAllocateBuffer
---

# WdsTransportServerAllocateBuffer function


## -description

Allocates a buffer in memory.

## -parameters

### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function.

### -param ulBufferSize [in]

Size of the buffer to be allocated.