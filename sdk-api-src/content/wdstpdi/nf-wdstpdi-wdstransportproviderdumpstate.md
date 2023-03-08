---
UID: NF:wdstpdi.WdsTransportProviderDumpState
title: WdsTransportProviderDumpState function (wdstpdi.h)
description: Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.
helpviewer_keywords: ["WdsTransportProviderDumpState","WdsTransportProviderDumpState callback","WdsTransportProviderDumpState callback function [Windows Deployment Services]","wds.wdstransportproviderdumpstate","wdstpdi/WdsTransportProviderDumpState"]
old-location: wds\wdstransportproviderdumpstate.htm
tech.root: wds
ms.assetid: e7a7d866-2954-46fb-8356-dbd7761efcf3
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderDumpState, WdsTransportProviderDumpState callback, WdsTransportProviderDumpState callback function [Windows Deployment Services], wds.wdstransportproviderdumpstate, wdstpdi/WdsTransportProviderDumpState
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsTransportProviderDumpState
 - wdstpdi/WdsTransportProviderDumpState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderDumpState
---

# WdsTransportProviderDumpState function


## -description

Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.



## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is optional.

