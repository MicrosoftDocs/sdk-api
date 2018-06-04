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

# _SSortOrderSet structure


## -description


Do not use. Defines a collection of  keys for a table to be used for standard or categorized sorting.


## -struct-fields




### -field cSorts

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifes the number of <a href="https://msdn.microsoft.com/7f8d7ccc-6f20-42fc-bb60-0d3449192c9e">SSortOrder</a> structures that are included in the <b>aSort</b> member. 



### -field cCategories

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifes the number of columns that are designated as category columns. Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the <b>cSorts</b> member.


### -field cExpanded

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of categories that start in an expanded state, where all the rows that apply to the category are visible in the table view. Possible values range from zero to the number indicated by <b>cCategories</b>. 



### -field aSort

Type: <b><a href="https://msdn.microsoft.com/7f8d7ccc-6f20-42fc-bb60-0d3449192c9e">SSortOrder</a>[MAPI_DIM]</b>

Array of variables of type <a href="https://msdn.microsoft.com/7f8d7ccc-6f20-42fc-bb60-0d3449192c9e">SSortOrder</a> that specifies the structures that define a sort order.

