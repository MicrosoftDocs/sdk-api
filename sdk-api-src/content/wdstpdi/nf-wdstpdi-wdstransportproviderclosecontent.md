---
UID: NF:wdstpdi.WdsTransportProviderCloseContent
title: WdsTransportProviderCloseContent function
author: windows-sdk-content
description: Closes a content stream specified by a handle.
old-location: wds\wdstransportproviderclosecontent.htm
old-project: Wds
ms.assetid: 358fdf14-b57b-4c07-b0a5-d8f49aa96c21
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WdsTransportProviderCloseContent, WdsTransportProviderCloseContent callback, WdsTransportProviderCloseContent callback function [Windows Deployment Services], wds.wdstransportproviderclosecontent, wdstpdi/WdsTransportProviderCloseContent
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	wdstpdi.h
api_name:
-	WdsTransportProviderCloseContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



