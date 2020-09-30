---
UID: NF:wdstpdi.WdsTransportProviderCloseInstance
title: WdsTransportProviderCloseInstance function (wdstpdi.h)
description: Closes an instance of a content provider specified by a handle.
helpviewer_keywords: ["WdsTransportProviderCloseInstance","WdsTransportProviderCloseInstance callback","WdsTransportProviderCloseInstance callback function [Windows Deployment Services]","wds.wdstransportprovidercloseinstance","wdstpdi/WdsTransportProviderCloseInstance"]
old-location: wds\wdstransportprovidercloseinstance.htm
tech.root: wds
ms.assetid: 3eb0a931-ca5d-4db4-9c40-9c52f98be429
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderCloseInstance, WdsTransportProviderCloseInstance callback, WdsTransportProviderCloseInstance callback function [Windows Deployment Services], wds.wdstransportprovidercloseinstance, wdstpdi/WdsTransportProviderCloseInstance
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
 - WdsTransportProviderCloseInstance
 - wdstpdi/WdsTransportProviderCloseInstance
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
 - WdsTransportProviderCloseInstance
---

# WdsTransportProviderCloseInstance function


## -description

Closes an instance of a content provider specified by a handle.

## -parameters

### -param hInstance [in]

Handle to the content provider instance to be closed.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.

