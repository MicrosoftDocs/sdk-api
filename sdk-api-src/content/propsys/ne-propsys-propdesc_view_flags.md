---
UID: NE:propsys.PROPDESC_VIEW_FLAGS
title: PROPDESC_VIEW_FLAGS (propsys.h)
author: windows-sdk-content
description: These flags describe properties in property description list strings.
old-location: properties\PROPDESC_VIEW_FLAGS.htm
tech.root: properties
ms.assetid: 8b38d085-180b-47c1-b703-8c4feaaa9ccb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PDVF_BEGINNEWGROUP, PDVF_CANWRAP, PDVF_CENTERALIGN, PDVF_DEFAULT, PDVF_FILLAREA, PDVF_HIDDEN, PDVF_HIDELABEL, PDVF_MASK_ALL, PDVF_RIGHTALIGN, PDVF_SHOWBYDEFAULT, PDVF_SHOWINPRIMARYLIST, PDVF_SHOWINSECONDARYLIST, PDVF_SHOWONLYIFPRESENT, PDVF_SORTDESCENDING, PROPDESC_VIEW_FLAGS, PROPDESC_VIEW_FLAGS enumeration [Windows Properties], properties.PROPDESC_VIEW_FLAGS, propsys/PDVF_BEGINNEWGROUP, propsys/PDVF_CANWRAP, propsys/PDVF_CENTERALIGN, propsys/PDVF_DEFAULT, propsys/PDVF_FILLAREA, propsys/PDVF_HIDDEN, propsys/PDVF_HIDELABEL, propsys/PDVF_MASK_ALL, propsys/PDVF_RIGHTALIGN, propsys/PDVF_SHOWBYDEFAULT, propsys/PDVF_SHOWINPRIMARYLIST, propsys/PDVF_SHOWINSECONDARYLIST, propsys/PDVF_SHOWONLYIFPRESENT, propsys/PDVF_SORTDESCENDING, propsys/PROPDESC_VIEW_FLAGS, shell.PROPDESC_VIEW_FLAGS, shell_PROPDESC_VIEW_FLAGS
ms.topic: enum
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - PROPDESC_VIEW_FLAGS
product: Windows
targetos: Windows
req.typenames: PROPDESC_VIEW_FLAGS
req.redist: 
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



