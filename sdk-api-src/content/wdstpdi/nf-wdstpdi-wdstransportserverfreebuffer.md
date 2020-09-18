---
UID: NF:wdstpdi.WdsTransportServerFreeBuffer
title: WdsTransportServerFreeBuffer function (wdstpdi.h)
description: Releases memory used by a buffer.
helpviewer_keywords: ["WdsTransportServerFreeBuffer","WdsTransportServerFreeBuffer function [Windows Deployment Services]","wds.wdstransportserverfreebuffer","wdstpdi/WdsTransportServerFreeBuffer"]
old-location: wds\wdstransportserverfreebuffer.htm
tech.root: wds
ms.assetid: c6123cec-fed3-4745-9d82-e501e972d54f
ms.date: 12/05/2018
ms.keywords: WdsTransportServerFreeBuffer, WdsTransportServerFreeBuffer function [Windows Deployment Services], wds.wdstransportserverfreebuffer, wdstpdi/WdsTransportServerFreeBuffer
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
 - WdsTransportServerFreeBuffer
 - wdstpdi/WdsTransportServerFreeBuffer
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
 - WdsTransportServerFreeBuffer
---

# WdsTransportServerFreeBuffer function


## -description

Releases memory used by  a buffer.

## -parameters

### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function.

### -param pvBuffer [in]

Pointer to location of buffer to be released.

## -returns

If the function succeeds, the return is <b>S_OK</b>.