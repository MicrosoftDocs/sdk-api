---
UID: NF:wdstpdi.WdsTransportProviderCompareContent
title: WdsTransportProviderCompareContent function (wdstpdi.h)
author: windows-sdk-content
description: Compares a specified content name and instance to an open content stream to determine if they are the same.
old-location: wds\wdstransportprovidercomparecontent.htm
tech.root: wds
ms.assetid: 206b85e2-e139-4f62-9107-ed78893a7ad2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsTransportProviderCompareContent, WdsTransportProviderCompareContent callback, WdsTransportProviderCompareContent callback function [Windows Deployment Services], wds.wdstransportprovidercomparecontent, wdstpdi/WdsTransportProviderCompareContent
ms.topic: function
f1_keywords: 
 - "wdstpdi/WdsTransportProviderCompareContent"
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
 - WdsTransportProviderCompareContent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



