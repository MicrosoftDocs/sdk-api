---
UID: NF:wdstpdi.WdsTransportProviderGetContentSize
title: WdsTransportProviderGetContentSize function
author: windows-sdk-content
description: Retrieves the size of an open content stream.
old-location: wds\wdstransportprovidergetcontentsize.htm
old-project: wds
ms.assetid: 2ab55723-b55a-454e-92f8-164a07c86028
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsTransportProviderGetContentSize, WdsTransportProviderGetContentSize callback, WdsTransportProviderGetContentSize callback function [Windows Deployment Services], wds.wdstransportprovidergetcontentsize, wdstpdi/WdsTransportProviderGetContentSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WdsTransportProviderGetContentSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportProviderGetContentSize function


## -description


Retrieves the size of an open content stream. 


## -parameters




### -param hContent [in]

Handle to an open content stream, opened with the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param pContentSize [out]

Pointer to a large integer that receives the size of the content stream. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



