---
UID: NF:wdsbp.WdsBpAddOption
title: WdsBpAddOption function (wdsbp.h)

description: Adds an option to the packet.
old-location: wds\wdsbpaddoption.htm
tech.root: wds
ms.assetid: 4418fe47-4d54-4874-9ab1-6747f9d9eb72

ms.date: 12/05/2018
ms.keywords: WdsBpAddOption, WdsBpAddOption function [Windows Deployment Services], wds.wdsbpaddoption, wdsbp/WdsBpAddOption
ms.topic: function
f1_keywords: 
 - "wdsbp/WdsBpAddOption"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsBpAddOption function


## -description


Adds an option to the packet.


## -parameters




### -param hHandle [in]

A handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpinitialize">WdsBpInitialize</a> function.


### -param uOption [in]

Specifies the option to add to the packet.


### -param uValueLen [in]

The length, in bytes, for the value.


### -param pValue [in]

A pointer to a location that contains the value for the option.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



