---
UID: NF:wdstpdi.WdsTransportServerTrace
title: WdsTransportServerTrace function (wdstpdi.h)
author: windows-sdk-content
description: Sends a debugging message.
old-location: wds\wdstransportservertrace.htm
tech.root: wds
ms.assetid: 6b0d6b1a-4a77-43f8-affd-6489f9a65050
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WDS_MC_TRACE_ERROR, WDS_MC_TRACE_FATAL, WDS_MC_TRACE_INFO, WDS_MC_TRACE_VERBOSE, WDS_MC_TRACE_WARNING, WdsTransportServerTrace, WdsTransportServerTrace function [Windows Deployment Services], wds.wdstransportservertrace, wdstpdi/WdsTransportServerTrace
ms.topic: function
f1_keywords: 
 - "wdstpdi/WdsTransportServerTrace"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsmc.dll
api_name:
 - WdsTransportServerTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsTransportServerTrace function


## -description


Sends a  debugging message.


## -parameters




### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="https://docs.microsoft.com/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function. 


### -param Severity [in]

Severity level of the message.



#### WDS_MC_TRACE_VERBOSE (0x00010000)



#### WDS_MC_TRACE_INFO (0x00020000)



#### WDS_MC_TRACE_WARNING (0x00040000)



#### WDS_MC_TRACE_ERROR (0x00080000)



#### WDS_MC_TRACE_FATAL (0x00010000)


### -param pwszFormat [in]

A pointer to a null-terminated string value that contains a formatted string. 


### -param arg4

TBD




## -returns



If the function succeeds, the return is <b>S_OK</b>.



