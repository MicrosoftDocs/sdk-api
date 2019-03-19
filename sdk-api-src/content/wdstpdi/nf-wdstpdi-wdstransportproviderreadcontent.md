---
UID: NF:wdstpdi.WdsTransportProviderReadContent
title: WdsTransportProviderReadContent function (wdstpdi.h)
author: windows-sdk-content
description: Reads content from an open content stream.
old-location: wds\wdstransportproviderreadcontent.htm
tech.root: wds
ms.assetid: 2b208871-a623-469b-a5dc-40d0c8009c02
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WdsTransportProviderReadContent, WdsTransportProviderReadContent callback, WdsTransportProviderReadContent callback function [Windows Deployment Services], wds.wdstransportproviderreadcontent, wdstpdi/WdsTransportProviderReadContent
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
 - WdsTransportProviderReadContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsTransportProviderReadContent function


## -description


Reads content from an open content stream. 


## -parameters




### -param hContent [in]

Handle to an open content stream to be read. This is the handle return by the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param pBuffer [in]

Pointer to location to receive read content.


### -param ulBytesToRead [in]

The size in bytes of the buffer at the location specified by the <i>pBuffer</i> parameter.


### -param pContentOffset [in]

The offset into the content stream specified by <i>hContent</i> from which to start reading.


### -param pvUserData [in]

User specified data passed to the callback function.  


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



