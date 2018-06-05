---
UID: NF:wdstpdi.WdsTransportProviderCompareContent
title: WdsTransportProviderCompareContent function
author: windows-sdk-content
description: Compares a specified content name and instance to an open content stream to determine if they are the same.
old-location: wds\wdstransportprovidercomparecontent.htm
old-project: Wds
ms.assetid: 206b85e2-e139-4f62-9107-ed78893a7ad2
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WdsTransportProviderCompareContent, WdsTransportProviderCompareContent callback, WdsTransportProviderCompareContent callback function [Windows Deployment Services], wds.wdstransportprovidercomparecontent, wdstpdi/WdsTransportProviderCompareContent
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
-	WdsTransportProviderCompareContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsTransportProviderCompareContent function


## -description


Compares a specified content name and instance to an open content stream to determine if they are the same. 


## -parameters




### -param hInstance [in]

Handle to an instance against which this content will be opened.


### -param pwszContentName [in]

The name of the content to compare.


### -param hContent [in]

Handle to a  open content stream.


### -param pbContentMatches [out]

If the content stream identified to by <i>hInstance</i> and <i>pwszContentName</i> is exactly the same as the content stream specified by  <i>hContent</i>, the location receives a true value. Otherwise, the location receives a false value.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



