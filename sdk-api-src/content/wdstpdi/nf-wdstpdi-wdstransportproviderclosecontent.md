---
UID: NF:wdstpdi.WdsTransportProviderCloseContent
title: WdsTransportProviderCloseContent function (wdstpdi.h)
description: Closes a content stream specified by a handle.
helpviewer_keywords: ["WdsTransportProviderCloseContent","WdsTransportProviderCloseContent callback","WdsTransportProviderCloseContent callback function [Windows Deployment Services]","wds.wdstransportproviderclosecontent","wdstpdi/WdsTransportProviderCloseContent"]
old-location: wds\wdstransportproviderclosecontent.htm
tech.root: wds
ms.assetid: 358fdf14-b57b-4c07-b0a5-d8f49aa96c21
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderCloseContent, WdsTransportProviderCloseContent callback, WdsTransportProviderCloseContent callback function [Windows Deployment Services], wds.wdstransportproviderclosecontent, wdstpdi/WdsTransportProviderCloseContent
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
 - WdsTransportProviderCloseContent
 - wdstpdi/WdsTransportProviderCloseContent
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
 - WdsTransportProviderCloseContent
---

# WdsTransportProviderCloseContent function


## -description

Closes a content stream specified by a handle.

## -parameters

### -param hContent [in]

Handle to the content stream to be closed.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.

