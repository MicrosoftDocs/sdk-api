---
UID: NF:wdstpdi.WdsTransportProviderInitialize
title: WdsTransportProviderInitialize function
author: windows-sdk-content
description: Initializes a content provider.
old-location: wds\wdstransportproviderinitialize.htm
old-project: Wds
ms.assetid: b7592e8d-6d7d-426a-8520-7b9cc5810d5a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WdsTransportProviderInitialize, WdsTransportProviderInitialize callback, WdsTransportProviderInitialize callback function [Windows Deployment Services], wds.wdstransportproviderinitialize, wdstpdi/WdsTransportProviderInitialize
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
 - WdsTransportProviderInitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



