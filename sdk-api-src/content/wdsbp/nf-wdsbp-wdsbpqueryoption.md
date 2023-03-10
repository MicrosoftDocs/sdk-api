---
UID: NF:wdsbp.WdsBpQueryOption
title: WdsBpQueryOption function (wdsbp.h)
description: Returns the value of an option from the parsed packet.
helpviewer_keywords: ["WdsBpQueryOption","WdsBpQueryOption function [Windows Deployment Services]","wds.wdsbpqueryoption","wdsbp/WdsBpQueryOption"]
old-location: wds\wdsbpqueryoption.htm
tech.root: wds
ms.assetid: 98c0d220-db20-4aba-9df0-e50f3b947da2
ms.date: 12/05/2018
ms.keywords: WdsBpQueryOption, WdsBpQueryOption function [Windows Deployment Services], wds.wdsbpqueryoption, wdsbp/WdsBpQueryOption
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsBpQueryOption
 - wdsbp/WdsBpQueryOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpQueryOption
---

# WdsBpQueryOption function


## -description

Returns the value of an option from the parsed packet.

## -parameters

### -param hHandle [in]

A handle returned by the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpparseinitialize">WdsBpParseInitialize</a> function.

### -param uOption [in]

Specifies the option to add to the packet.

### -param uValueLen [out]

The total number of bytes of memory pointed to by the <i>pValue</i> parameter. To determine the number of bytes required to store the value for the option, set <i>uValueLen</i> to zero and <i>pValue</i> to <b>NULL</b>; the <b>WdsBpQueryOption</b> function returns <b>ERROR_INSUFFICIENT_BUFFER</b>, and the location pointed to by the <i>puBytes</i> parameter receives the number of bytes required for the value.

### -param pValue [out]

The value of the option is returned in this buffer.

### -param puBytes [out]

If the buffer is large enough for the value, this parameter receives the number of bytes copied to <i>pValue</i>. If not enough space is available, this parameter receives the total number of bytes required to store the value.

## -returns

If the function succeeds, the return is <b>S_OK</b>.