---
UID: NF:wdstpdi.WdsTransportProviderGetContentMetadata
title: WdsTransportProviderGetContentMetadata function (wdstpdi.h)
description: Retrieves metadata for an open content stream.
helpviewer_keywords: ["WdsTransportProviderGetContentMetadata","WdsTransportProviderGetContentMetadata callback","WdsTransportProviderGetContentMetadata callback function [Windows Deployment Services]","wds.wdstransportprovidergetcontentmetadata","wdstpdi/WdsTransportProviderGetContentMetadata"]
old-location: wds\wdstransportprovidergetcontentmetadata.htm
tech.root: wds
ms.assetid: ed243373-b5ff-418d-811c-544589ea11ac
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderGetContentMetadata, WdsTransportProviderGetContentMetadata callback, WdsTransportProviderGetContentMetadata callback function [Windows Deployment Services], wds.wdstransportprovidergetcontentmetadata, wdstpdi/WdsTransportProviderGetContentMetadata
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
 - WdsTransportProviderGetContentMetadata
 - wdstpdi/WdsTransportProviderGetContentMetadata
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
 - WdsTransportProviderGetContentMetadata
---

# WdsTransportProviderGetContentMetadata function


## -description

Retrieves metadata for an open content stream.

## -parameters

### -param hContent [in]

Handle to an open content stream, opened with the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent">WdsTransportProviderOpenContent</a> callback.

### -param pvData [out]

Pointer to the location in memory to receive content metadata.

### -param pulLength [out]

The size of the buffer located at <i>pvData</i> in bytes.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.