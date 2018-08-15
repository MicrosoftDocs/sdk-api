---
UID: NF:wdstpdi.WdsTransportProviderGetContentMetadata
title: WdsTransportProviderGetContentMetadata function
author: windows-sdk-content
description: Retrieves metadata for an open content stream.
old-location: wds\wdstransportprovidergetcontentmetadata.htm
old-project: wds
ms.assetid: ed243373-b5ff-418d-811c-544589ea11ac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsTransportProviderGetContentMetadata, WdsTransportProviderGetContentMetadata callback, WdsTransportProviderGetContentMetadata callback function [Windows Deployment Services], wds.wdstransportprovidergetcontentmetadata, wdstpdi/WdsTransportProviderGetContentMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdstpdi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRANSPORTPROVIDER_CALLBACK_ID, *PTRANSPORTPROVIDER_CALLBACK_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wdstpdi.h
api_name:
 - WdsTransportProviderGetContentMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportProviderGetContentMetadata function


## -description


Retrieves metadata for an open content stream.


## -parameters




### -param hContent [in]

Handle to an open content stream, opened with the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param pvData [out]

Pointer to the location in memory to receive content metadata.


### -param pulLength [out]

The size of the buffer located at <i>pvData</i> in bytes.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



