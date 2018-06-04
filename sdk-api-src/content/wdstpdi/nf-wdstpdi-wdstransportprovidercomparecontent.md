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



