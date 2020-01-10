---
UID: NF:wdstpdi.WdsTransportProviderOpenContent
title: WdsTransportProviderOpenContent function (wdstpdi.h)
description: Opens a new static view of a content stream.
old-location: wds\wdstransportprovideropencontent.htm
tech.root: wds
ms.assetid: 95bea971-9c97-4d66-871d-5ef7407b9659
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderOpenContent, WdsTransportProviderOpenContent callback, WdsTransportProviderOpenContent callback function [Windows Deployment Services], wds.wdstransportprovideropencontent, wdstpdi/WdsTransportProviderOpenContent
f1_keywords:
- wdstpdi/WdsTransportProviderOpenContent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- wdstpdi.h
api_name:
- WdsTransportProviderOpenContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsTransportProviderOpenContent function


## -description


Opens a new static view of a content stream.


## -parameters




### -param hInstance [in]

Handle to the instance against which this content will be opened. 


### -param pwszContentName [in]

The name of the content stream.


### -param phContent [out]

Pointer to a handle that identifies this content stream to the provider. 




## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.

When the handle returned by this function is no longer needed it should be closed with using the <a href="https://docs.microsoft.com/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent">WdsTransportProviderCloseContent</a> callback.



