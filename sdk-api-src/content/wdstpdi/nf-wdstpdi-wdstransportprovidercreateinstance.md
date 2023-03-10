---
UID: NF:wdstpdi.WdsTransportProviderCreateInstance
title: WdsTransportProviderCreateInstance function (wdstpdi.h)
description: Opens a new instance of a content provider.
helpviewer_keywords: ["WdsTransportProviderCreateInstance","WdsTransportProviderCreateInstance callback","WdsTransportProviderCreateInstance callback function [Windows Deployment Services]","wds.wdstransportprovidercreateinstance","wdstpdi/WdsTransportProviderCreateInstance"]
old-location: wds\wdstransportprovidercreateinstance.htm
tech.root: wds
ms.assetid: 534ba680-e5d7-47e7-83ad-2b621feab99f
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderCreateInstance, WdsTransportProviderCreateInstance callback, WdsTransportProviderCreateInstance callback function [Windows Deployment Services], wds.wdstransportprovidercreateinstance, wdstpdi/WdsTransportProviderCreateInstance
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
 - WdsTransportProviderCreateInstance
 - wdstpdi/WdsTransportProviderCreateInstance
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
 - WdsTransportProviderCreateInstance
---

# WdsTransportProviderCreateInstance function


## -description

Opens a new instance of a content provider.

## -parameters

### -param pwszConfigString [in]

Configuration information for this instance of the content provider.

### -param phInstance [out]

Receives a pointer to a handle that identifies this instance.  When the instance is no longer needed, the handle should be closed with the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance">WdsTransportProviderCloseInstance</a> callback.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.