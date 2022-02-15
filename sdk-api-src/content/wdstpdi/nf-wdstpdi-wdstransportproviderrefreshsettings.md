---
UID: NF:wdstpdi.WdsTransportProviderRefreshSettings
title: WdsTransportProviderRefreshSettings function (wdstpdi.h)
description: Instructs the transport provider to reread any relevant settings.
helpviewer_keywords: ["WdsTransportProviderRefreshSettings","WdsTransportProviderRefreshSettings callback","WdsTransportProviderRefreshSettings callback function [Windows Deployment Services]","wds.wdstransportproviderrefreshsettings","wdstpdi/WdsTransportProviderRefreshSettings"]
old-location: wds\wdstransportproviderrefreshsettings.htm
tech.root: wds
ms.assetid: b5fc2340-6820-4b11-b96b-dcf3186f0786
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderRefreshSettings, WdsTransportProviderRefreshSettings callback, WdsTransportProviderRefreshSettings callback function [Windows Deployment Services], wds.wdstransportproviderrefreshsettings, wdstpdi/WdsTransportProviderRefreshSettings
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
 - WdsTransportProviderRefreshSettings
 - wdstpdi/WdsTransportProviderRefreshSettings
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
 - WdsTransportProviderRefreshSettings
---

# WdsTransportProviderRefreshSettings function


## -description

Instructs the transport provider to reread any relevant settings.



## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is optional.

