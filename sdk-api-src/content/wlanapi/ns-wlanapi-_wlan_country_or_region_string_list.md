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

# _WLAN_COUNTRY_OR_REGION_STRING_LIST structure


## -description


A <b>WLAN_COUNTRY_OR_REGION_STRING_LIST</b> structure contains a list of supported country or region strings.


## -struct-fields




### -field dwNumberOfItems

Indicates the number of supported country or region strings.


### -field pCountryOrRegionStringList.unique

 


### -field pCountryOrRegionStringList.size_is

 


### -field pCountryOrRegionStringList.size_is.dwNumberOfItems

 


### -field pCountryOrRegionStringList

A list of supported country or region strings. In Windows, a <b>DOT11_COUNTRY_OR_REGION_STRING</b> is of type <b>char[3]</b>.


## -see-also




<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

