---
UID: NS:wabdefs._SSortOrderSet
title: SSortOrderSet
author: windows-sdk-content
description: Do not use. Defines a collection of keys for a table to be used for standard or categorized sorting.
old-location: wab\_wab_SSortOrderSet.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\ssortorderset.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSSortOrderSet, LPSSortOrderSet, LPSSortOrderSet structure pointer [Windows Address Book], SSortOrderSet, SSortOrderSet structure [Windows Address Book], _wab_SSortOrderSet, wab._wab_SSortOrderSet, wabdefs/LPSSortOrderSet, wabdefs/SSortOrderSet"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SSortOrderSet
product: Windows
targetos: Windows
req.typenames: SSortOrderSet, *LPSSortOrderSet
req.redist: 
req.product: Internet Explorer 4.0
---

# SSortOrderSet structure


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

