---
UID: NF:wdsclientapi.WdsCliRegisterTrace
title: WdsCliRegisterTrace function (wdsclientapi.h)
author: windows-sdk-content
description: Registers a callback function that will receive debugging messages.
old-location: wds\wdscliregistertrace.htm
tech.root: wds
ms.assetid: 1bdb1e47-fbbb-4952-9339-accdfe40bd18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliRegisterTrace, WdsCliRegisterTrace function [Windows Deployment Services], wds.wdscliregistertrace, wdsclientapi/WdsCliRegisterTrace
ms.topic: function
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
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliRegisterTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliRegisterTrace function


## -description


Registers a callback function that will receive debugging messages.


## -parameters




### -param pfn [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/5c10c767-45d2-4b42-b7c3-a2cd8188975e">PFN_WdsCliTraceFunction</a> callback function that receives debugging messages.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



