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

# SORTCOLUMN structure


## -description


Stores information about how to sort a column that is displayed in the folder view.


## -struct-fields




### -field propkey

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a></b>

The ID of the column by which the user will sort. A <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure. For example, for the "Name" column, the property key is PKEY_ItemNameDisplay.


### -field direction

Type: <b>SORTDIRECTION</b>

The direction in which the items are sorted. One of the following values.



#### SORT_DESCENDING

The items are sorted in ascending order. Whether the sort is alphabetical, numerical, and so on, is determined by the data type of the column indicated in <b>propkey</b>.



#### SORT_ASCENDING

The items are sorted in descending order. Whether the sort is alphabetical, numerical, and so on, is determined by the data type of the column indicated in <b>propkey</b>.


## -remarks



Each column displayed in the folder view (for example, "details" view mode), is associated with a property that has a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> ID. When you want to sort the view by a particular property, you specify the property key for that property.



