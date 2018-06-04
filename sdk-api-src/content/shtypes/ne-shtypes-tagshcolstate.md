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

# tagSHCOLSTATE enumeration


## -description


Describes how a property should be treated. These values are defined in Shtypes.h.


## -enum-fields




### -field SHCOLSTATE_DEFAULT

The value is displayed according to default settings for the column.


### -field SHCOLSTATE_TYPE_STR

The value is displayed as a string.


### -field SHCOLSTATE_TYPE_INT

The value is displayed as an integer.


### -field SHCOLSTATE_TYPE_DATE

The value is displayed as a date/time.


### -field SHCOLSTATE_TYPEMASK

A mask for display type values SHCOLSTATE_TYPE_STR, SHCOLSTATE_TYPE_STR, and SHCOLSTATE_TYPE_DATE.


### -field SHCOLSTATE_ONBYDEFAULT

The column should be on by default in Details view.


### -field SHCOLSTATE_SLOW

Will be slow to compute. Perform on a background thread.


### -field SHCOLSTATE_EXTENDED

Provided by a handler, not the folder.


### -field SHCOLSTATE_SECONDARYUI

Not displayed in the context menu, but is listed in the <b>More...</b> dialog.


### -field SHCOLSTATE_HIDDEN

Not displayed in the UI.


### -field SHCOLSTATE_PREFER_VARCMP

<b>VarCmp</b> produces same result as <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">IShellFolder::CompareIDs</a>.


### -field SHCOLSTATE_PREFER_FMTCMP


<a href="https://msdn.microsoft.com/71442967-ee8a-448c-83cf-949934ddd152">PSFormatForDisplay</a> produces same result as <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">IShellFolder::CompareIDs</a>.


### -field SHCOLSTATE_NOSORTBYFOLDERNESS

Do not sort folders separately.


### -field SHCOLSTATE_VIEWONLY

Only displayed in the UI.


### -field SHCOLSTATE_BATCHREAD

Marks columns with values that should be read in a batch.


### -field SHCOLSTATE_NO_GROUPBY

Grouping is disabled for this column.


### -field SHCOLSTATE_FIXED_WIDTH

Can't resize the column.


### -field SHCOLSTATE_NODPISCALE

The width is the same in all dpi.


### -field SHCOLSTATE_FIXED_RATIO

Fixed width and height ratio.


### -field SHCOLSTATE_DISPLAYMASK

Filters out new display flags.

