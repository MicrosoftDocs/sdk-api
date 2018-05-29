---
UID: NC:wdsclientapi.PFN_WdsCliTraceFunction
title: PFN_WdsCliTraceFunction
author: windows-sdk-content
description: Defines a callback function that can receive debugging messages from the WDS client.
old-location: wds\pfn_wdsclitracefunction.htm
old-project: Wds
ms.assetid: 5c10c767-45d2-4b42-b7c3-a2cd8188975e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PFN_WdsCliTraceFunction, PFN_WdsCliTraceFunction callback, PFN_WdsCliTraceFunction callback function [Windows Deployment Services], wds.pfn_wdsclitracefunction, wdsclientapi/PFN_WdsCliTraceFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WAITCHAIN_NODE_INFO, *PWAITCHAIN_NODE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WdsClientAPI.h
api_name:
-	PFN_WdsCliTraceFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_WdsCliTraceFunction callback function


## -description


Defines a callback function that can receive debugging messages from the WDS client.


## -parameters




### -param pwszFormat [in]

A pointer to a null-terminated string value that contains a formatted string.


### -param Params [in]

A list of parameters used by the formatted string.


## -returns



This callback function does not return a value.



