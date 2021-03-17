---
UID: NF:wdstpdi.WdsTransportServerRegisterCallback
title: WdsTransportServerRegisterCallback function (wdstpdi.h)
description: Registers a provider callback with the multicast server.
helpviewer_keywords: ["WdsTransportServerRegisterCallback","WdsTransportServerRegisterCallback function [Windows Deployment Services]","wds.wdstransportserverregistercallback","wdstpdi/WdsTransportServerRegisterCallback"]
old-location: wds\wdstransportserverregistercallback.htm
tech.root: wds
ms.assetid: 565ceb6c-0e44-4c71-8b67-092cd33d088e
ms.date: 12/05/2018
ms.keywords: WdsTransportServerRegisterCallback, WdsTransportServerRegisterCallback function [Windows Deployment Services], wds.wdstransportserverregistercallback, wdstpdi/WdsTransportServerRegisterCallback
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
 - WdsTransportServerRegisterCallback
 - wdstpdi/WdsTransportServerRegisterCallback
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
 - WdsTransportServerRegisterCallback
---

# WdsTransportServerRegisterCallback function


## -description

Registers a provider callback with the multicast server.

## -parameters

### -param hProvider [in]

Handle to the provider. This handle was given to the provider in the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize">WdsTransportProviderInitialize</a> function.

### -param CallbackId [in]

The value of this parameter is a <a href="/windows/desktop/api/wdstpdi/ne-wdstpdi-transportprovider_callback_id">TRANSPORTPROVIDER_CALLBACK_ID</a> structure.

### -param pfnCallback [in]

Pointer to the function pointer associated with this id.

## -returns

If the function succeeds, the return is <b>S_OK</b>.