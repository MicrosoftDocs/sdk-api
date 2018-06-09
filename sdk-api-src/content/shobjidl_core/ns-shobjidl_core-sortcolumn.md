---
UID: NS:shobjidl_core.SORTCOLUMN
title: SORTCOLUMN
author: windows-sdk-content
description: Stores information about how to sort a column that is displayed in the folder view.
old-location: shell\SORTCOLUMN.htm
old-project: shell
ms.assetid: 3ca4c318-6462-4e22-813c-ef7b3ef03230
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SORTCOLUMN, SORTCOLUMN structure [Windows Shell], SORT_ASCENDING, SORT_DESCENDING, _shell_SORTCOLUMN, shell.SORTCOLUMN, shobjidl_core/SORTCOLUMN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SORTCOLUMN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SORTCOLUMN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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



