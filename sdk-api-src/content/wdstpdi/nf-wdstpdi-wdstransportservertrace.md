---
UID: NF:wdstpdi.WdsTransportServerTrace
title: WdsTransportServerTrace function
author: windows-sdk-content
description: Sends a debugging message.
old-location: wds\wdstransportservertrace.htm
old-project: Wds
ms.assetid: 6b0d6b1a-4a77-43f8-affd-6489f9a65050
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WDS_MC_TRACE_ERROR, WDS_MC_TRACE_FATAL, WDS_MC_TRACE_INFO, WDS_MC_TRACE_VERBOSE, WDS_MC_TRACE_WARNING, WdsTransportServerTrace, WdsTransportServerTrace function [Windows Deployment Services], wds.wdstransportservertrace, wdstpdi/WdsTransportServerTrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
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
req.lib: Wdsmc.lib
req.dll: Wdsmc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportServerTrace function


## -description


Sends a  debugging message.


## -parameters




### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="https://msdn.microsoft.com/b7592e8d-6d7d-426a-8520-7b9cc5810d5a">WdsTransportProviderInitialize</a> function. 


### -param Severity [in]

Severity level of the message.



#### WDS_MC_TRACE_VERBOSE (0x00010000)



#### WDS_MC_TRACE_INFO (0x00020000)



#### WDS_MC_TRACE_WARNING (0x00040000)



#### WDS_MC_TRACE_ERROR (0x00080000)



#### WDS_MC_TRACE_FATAL (0x00010000)


### -param pwszFormat [in]

A pointer to a null-terminated string value that contains a formatted string. 


### -param param

TBD




## -returns



If the function succeeds, the return is <b>S_OK</b>.



