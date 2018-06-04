---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WdsTransportProviderInitialize function


## -description


Initializes a content provider.


## -parameters




### -param pInParameters [in]

A pointer to a <a href="https://msdn.microsoft.com/5d89d192-7e60-4b5a-ba87-d5b30971a8a6">WDS_TRANSPORTPROVIDER_INIT_PARAMS</a> structure that informs the content provider about the server.


### -param pSettings [out]

A pointer to  a <a href="https://msdn.microsoft.com/334e86f2-97fa-4f64-93a4-b6aed6212eb1">WDS_TRANSPORTPROVIDER_SETTINGS</a> structure that informs the server about the content provider.


### -param ulLength [in]

The size in bytes of the buffer at the location specified by the <i>pSettings</i> parameter.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



