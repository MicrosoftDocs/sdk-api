---
UID: NF:wdstpdi.WdsTransportServerTrace
title: WdsTransportServerTrace function (wdstpdi.h)
description: Sends a debugging message. (WdsTransportServerTrace)
helpviewer_keywords: ["WDS_MC_TRACE_ERROR","WDS_MC_TRACE_FATAL","WDS_MC_TRACE_INFO","WDS_MC_TRACE_VERBOSE","WDS_MC_TRACE_WARNING","WdsTransportServerTrace","WdsTransportServerTrace function [Windows Deployment Services]","wds.wdstransportservertrace","wdstpdi/WdsTransportServerTrace"]
old-location: wds\wdstransportservertrace.htm
tech.root: wds
ms.assetid: 6b0d6b1a-4a77-43f8-affd-6489f9a65050
ms.date: 12/05/2018
ms.keywords: WDS_MC_TRACE_ERROR, WDS_MC_TRACE_FATAL, WDS_MC_TRACE_INFO, WDS_MC_TRACE_VERBOSE, WDS_MC_TRACE_WARNING, WdsTransportServerTrace, WdsTransportServerTrace function [Windows Deployment Services], wds.wdstransportservertrace, wdstpdi/WdsTransportServerTrace
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
 - WdsTransportServerTrace
 - wdstpdi/WdsTransportServerTrace
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
 - WdsTransportServerTrace
---

# WdsTransportServerTrace function


## -description

Sends a  debugging message.

## -parameters

### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function.

### -param Severity [in]

Severity level of the message.



#### WDS_MC_TRACE_VERBOSE (0x00010000)



#### WDS_MC_TRACE_INFO (0x00020000)



#### WDS_MC_TRACE_WARNING (0x00040000)



#### WDS_MC_TRACE_ERROR (0x00080000)



#### WDS_MC_TRACE_FATAL (0x00010000)

### -param pwszFormat [in]

A pointer to a null-terminated string value that contains a formatted string.

### -param ...

Additional arguments.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

