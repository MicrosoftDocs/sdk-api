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

# D2D1_HISTOGRAM_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/458E2334-F383-41DE-9479-601AC3007BF3">Histogram effect</a>.
        


## -enum-fields




### -field D2D1_HISTOGRAM_PROP_NUM_BINS

Specifies the number of bins used for the histogram. The range of intensity values that fall into a particular bucket depend on the number of specified buckets. 
          

The type is UINT32.

The default is 256.


### -field D2D1_HISTOGRAM_PROP_CHANNEL_SELECT

Specifies the channel used to generate the histogram. This effect has a single data output corresponding to the specified channel.
          

The type is <a href="https://msdn.microsoft.com/92BC07F7-4CB5-487E-9AFB-255C8EF1C6BA">D2D1_CHANNEL_SELECTOR</a>.

The default is D2D1_CHANNEL_SELECTOR_R.


### -field D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT

The output array.
          

The type is FLOAT[].


### -field D2D1_HISTOGRAM_PROP_FORCE_DWORD



