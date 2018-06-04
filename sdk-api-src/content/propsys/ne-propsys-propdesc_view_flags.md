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

# PROPDESC_VIEW_FLAGS enumeration


## -description


These flags describe properties in property description list strings.


## -enum-fields




### -field PDVF_DEFAULT

Show this property by default.


### -field PDVF_CENTERALIGN

This property should be centered.


### -field PDVF_RIGHTALIGN

This property should be right aligned.


### -field PDVF_BEGINNEWGROUP

Show this property as the beginning of the next collection of properties in the view.


### -field PDVF_FILLAREA

Fill the remainder of the view area with the content of this property.


### -field PDVF_SORTDESCENDING

Sort this property in reverse (descending) order. Applies to a property in a list of sorted properties.


### -field PDVF_SHOWONLYIFPRESENT

Show this property only if it is present.


### -field PDVF_SHOWBYDEFAULT

This property should be shown by default in a view (where applicable).


### -field PDVF_SHOWINPRIMARYLIST

This property should be shown by default in the primary column selection UI.


### -field PDVF_SHOWINSECONDARYLIST

This property should be shown by default in the secondary column selection UI.


### -field PDVF_HIDELABEL

Hide the label of this property if the view normally shows the label.


### -field PDVF_HIDDEN

This property should not be displayed as a column in the UI.


### -field PDVF_CANWRAP

This property can be wrapped to the next row.


### -field PDVF_MASK_ALL

A mask used to retrieve all flags.


## -remarks



These values are defined in propsys.h and propsys.idl.



