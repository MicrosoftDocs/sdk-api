---
UID: NF:wdstpdi.WdsTransportProviderInitialize
title: WdsTransportProviderInitialize function (wdstpdi.h)
description: Initializes a content provider.
helpviewer_keywords: ["WdsTransportProviderInitialize","WdsTransportProviderInitialize callback","WdsTransportProviderInitialize callback function [Windows Deployment Services]","wds.wdstransportproviderinitialize","wdstpdi/WdsTransportProviderInitialize"]
old-location: wds\wdstransportproviderinitialize.htm
tech.root: wds
ms.assetid: b7592e8d-6d7d-426a-8520-7b9cc5810d5a
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderInitialize, WdsTransportProviderInitialize callback, WdsTransportProviderInitialize callback function [Windows Deployment Services], wds.wdstransportproviderinitialize, wdstpdi/WdsTransportProviderInitialize
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
 - WdsTransportProviderInitialize
 - wdstpdi/WdsTransportProviderInitialize
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
 - WdsTransportProviderInitialize
---

# WdsTransportProviderInitialize function


## -description

Initializes a content provider.

## -parameters

### -param pInParameters [in]

A pointer to a <a href="/windows/desktop/api/wdstpdi/ns-wdstpdi-wds_transportprovider_init_params">WDS_TRANSPORTPROVIDER_INIT_PARAMS</a> structure that informs the content provider about the server.

### -param pSettings [out]

A pointer to  a <a href="/windows/desktop/api/wdstpdi/ns-wdstpdi-wds_transportprovider_settings">WDS_TRANSPORTPROVIDER_SETTINGS</a> structure that informs the server about the content provider.

### -param ulLength [in]

The size in bytes of the buffer at the location specified by the <i>pSettings</i> parameter.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.