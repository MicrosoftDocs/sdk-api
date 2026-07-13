---
UID: NF:wdstpdi.WdsTransportServerTraceV
title: WdsTransportServerTraceV function (wdstpdi.h)
description: Sends a debugging message. (WdsTransportServerTraceV)
helpviewer_keywords: ["WDS_MC_TRACE_ERROR","WDS_MC_TRACE_FATAL","WDS_MC_TRACE_INFO","WDS_MC_TRACE_VERBOSE","WDS_MC_TRACE_WARNING","WdsTransportServerTraceV","WdsTransportServerTraceV function [Windows Deployment Services]","wds.wdstransportservertracev","wdstpdi/WdsTransportServerTraceV"]
old-location: wds\wdstransportservertracev.htm
tech.root: wds
ms.assetid: d7b85bc4-0f8e-416d-848f-2486f979ac1b
ms.date: 12/05/2018
ms.keywords: WDS_MC_TRACE_ERROR, WDS_MC_TRACE_FATAL, WDS_MC_TRACE_INFO, WDS_MC_TRACE_VERBOSE, WDS_MC_TRACE_WARNING, WdsTransportServerTraceV, WdsTransportServerTraceV function [Windows Deployment Services], wds.wdstransportservertracev, wdstpdi/WdsTransportServerTraceV
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
 - WdsTransportServerTraceV
 - wdstpdi/WdsTransportServerTraceV
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
 - WdsTransportServerTraceV
---

# WdsTransportServerTraceV function


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

### -param Params [in]

A list of parameters used by the formatted string.

## -returns

If the function succeeds, the return is <b>S_OK</b>.
