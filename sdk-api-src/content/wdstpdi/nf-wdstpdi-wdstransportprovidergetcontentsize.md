---
UID: NF:wdstpdi.WdsTransportProviderGetContentSize
title: WdsTransportProviderGetContentSize function (wdstpdi.h)
description: Retrieves the size of an open content stream.
helpviewer_keywords: ["WdsTransportProviderGetContentSize","WdsTransportProviderGetContentSize callback","WdsTransportProviderGetContentSize callback function [Windows Deployment Services]","wds.wdstransportprovidergetcontentsize","wdstpdi/WdsTransportProviderGetContentSize"]
old-location: wds\wdstransportprovidergetcontentsize.htm
tech.root: wds
ms.assetid: 2ab55723-b55a-454e-92f8-164a07c86028
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderGetContentSize, WdsTransportProviderGetContentSize callback, WdsTransportProviderGetContentSize callback function [Windows Deployment Services], wds.wdstransportprovidergetcontentsize, wdstpdi/WdsTransportProviderGetContentSize
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
 - WdsTransportProviderGetContentSize
 - wdstpdi/WdsTransportProviderGetContentSize
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
 - WdsTransportProviderGetContentSize
---

# WdsTransportProviderGetContentSize function


## -description

Retrieves the size of an open content stream.

## -parameters

### -param hContent [in]

Handle to an open content stream, opened with the <a href="/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent">WdsTransportProviderOpenContent</a> callback.

### -param pContentSize [out]

Pointer to a large integer that receives the size of the content stream.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This callback is required.