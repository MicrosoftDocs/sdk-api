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

# _WSMAN_OPERATION_INFO structure


## -description


Represents a specific resource endpoint for which the plug-in must perform the request.


## -struct-fields




### -field fragment

A <a href="https://msdn.microsoft.com/2aa4ee38-6991-4f95-90fd-867b188fc9ff">WSMAN_FRAGMENT</a> structure that specifies the subset of data to be used for the operation. This parameter is reserved for future use and is ignored on receipt.


### -field filter

A <a href="https://msdn.microsoft.com/d99c11a8-e91f-428f-98b1-d3116d027691">WSMAN_FILTER</a> structure that specifies the filtering that is used for the operation. This parameter is reserved for future use and is ignored on receipt.


### -field selectorSet

A <a href="https://msdn.microsoft.com/8157c0e6-b992-46a9-9976-e57dd06e7f8b">WSMAN_SELECTOR_SET</a> structure that identifies the specific resource to use for the request.


### -field optionSet

A <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a> structure that specifies the set of options for the request.


### -field reserved

 


### -field version

 



