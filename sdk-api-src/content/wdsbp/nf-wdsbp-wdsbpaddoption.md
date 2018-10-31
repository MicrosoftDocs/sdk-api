---
UID: NF:wdsbp.WdsBpAddOption
title: WdsBpAddOption function
author: windows-sdk-content
description: Adds an option to the packet.
old-location: wds\wdsbpaddoption.htm
tech.root: wds
ms.assetid: 4418fe47-4d54-4874-9ab1-6747f9d9eb72
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WdsBpAddOption, WdsBpAddOption function [Windows Deployment Services], wds.wdsbpaddoption, wdsbp/WdsBpAddOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdsbp.h
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
req.lib: Wdsbp.lib
req.dll: Wdsbp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpAddOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsBpAddOption function


## -description


Adds an option to the packet.


## -parameters




### -param hHandle [in]

A handle returned by the <a href="https://msdn.microsoft.com/a77cbdf5-9025-4e98-8edd-1b9bae8493e7">WdsBpInitialize</a> function.


### -param uOption [in]

Specifies the option to add to the packet.


### -param uValueLen [in]

The length, in bytes, for the value.


### -param pValue [in]

A pointer to a location that contains the value for the option.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



