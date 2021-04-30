---
UID: NF:wdsbp.WdsBpCloseHandle
title: WdsBpCloseHandle function (wdsbp.h)
description: Closes the specified handle.
helpviewer_keywords: ["WdsBpCloseHandle","WdsBpCloseHandle function [Windows Deployment Services]","wds.wdsbpclosehandle","wdsbp/WdsBpCloseHandle"]
old-location: wds\wdsbpclosehandle.htm
tech.root: wds
ms.assetid: b35ec3e2-7dd5-4e17-b657-72bafe91921a
ms.date: 12/05/2018
ms.keywords: WdsBpCloseHandle, WdsBpCloseHandle function [Windows Deployment Services], wds.wdsbpclosehandle, wdsbp/WdsBpCloseHandle
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
 - WdsBpCloseHandle
 - wdsbp/WdsBpCloseHandle
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
 - WdsBpCloseHandle
---

# WdsBpCloseHandle function


## -description

Closes the specified handle.

## -parameters

### -param hHandle [in]

A handle to be closed. This can be a handle obtained using the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpparseinitialize">WdsBpParseInitialize</a> or <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpinitialize">WdsBpInitialize</a> functions.

## -returns

If the function succeeds, the return is <b>S_OK</b>.