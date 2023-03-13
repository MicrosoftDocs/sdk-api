---
UID: NE:propsys.PROPDESC_VIEW_FLAGS
title: PROPDESC_VIEW_FLAGS (propsys.h)
description: These flags describe properties in property description list strings.
helpviewer_keywords: ["PDVF_BEGINNEWGROUP","PDVF_CANWRAP","PDVF_CENTERALIGN","PDVF_DEFAULT","PDVF_FILLAREA","PDVF_HIDDEN","PDVF_HIDELABEL","PDVF_MASK_ALL","PDVF_RIGHTALIGN","PDVF_SHOWBYDEFAULT","PDVF_SHOWINPRIMARYLIST","PDVF_SHOWINSECONDARYLIST","PDVF_SHOWONLYIFPRESENT","PDVF_SORTDESCENDING","PROPDESC_VIEW_FLAGS","PROPDESC_VIEW_FLAGS enumeration [Windows Properties]","properties.PROPDESC_VIEW_FLAGS","propsys/PDVF_BEGINNEWGROUP","propsys/PDVF_CANWRAP","propsys/PDVF_CENTERALIGN","propsys/PDVF_DEFAULT","propsys/PDVF_FILLAREA","propsys/PDVF_HIDDEN","propsys/PDVF_HIDELABEL","propsys/PDVF_MASK_ALL","propsys/PDVF_RIGHTALIGN","propsys/PDVF_SHOWBYDEFAULT","propsys/PDVF_SHOWINPRIMARYLIST","propsys/PDVF_SHOWINSECONDARYLIST","propsys/PDVF_SHOWONLYIFPRESENT","propsys/PDVF_SORTDESCENDING","propsys/PROPDESC_VIEW_FLAGS","shell.PROPDESC_VIEW_FLAGS","shell_PROPDESC_VIEW_FLAGS"]
old-location: properties\PROPDESC_VIEW_FLAGS.htm
tech.root: properties
ms.assetid: 8b38d085-180b-47c1-b703-8c4feaaa9ccb
ms.date: 12/05/2018
ms.keywords: PDVF_BEGINNEWGROUP, PDVF_CANWRAP, PDVF_CENTERALIGN, PDVF_DEFAULT, PDVF_FILLAREA, PDVF_HIDDEN, PDVF_HIDELABEL, PDVF_MASK_ALL, PDVF_RIGHTALIGN, PDVF_SHOWBYDEFAULT, PDVF_SHOWINPRIMARYLIST, PDVF_SHOWINSECONDARYLIST, PDVF_SHOWONLYIFPRESENT, PDVF_SORTDESCENDING, PROPDESC_VIEW_FLAGS, PROPDESC_VIEW_FLAGS enumeration [Windows Properties], properties.PROPDESC_VIEW_FLAGS, propsys/PDVF_BEGINNEWGROUP, propsys/PDVF_CANWRAP, propsys/PDVF_CENTERALIGN, propsys/PDVF_DEFAULT, propsys/PDVF_FILLAREA, propsys/PDVF_HIDDEN, propsys/PDVF_HIDELABEL, propsys/PDVF_MASK_ALL, propsys/PDVF_RIGHTALIGN, propsys/PDVF_SHOWBYDEFAULT, propsys/PDVF_SHOWINPRIMARYLIST, propsys/PDVF_SHOWINSECONDARYLIST, propsys/PDVF_SHOWONLYIFPRESENT, propsys/PDVF_SORTDESCENDING, propsys/PROPDESC_VIEW_FLAGS, shell.PROPDESC_VIEW_FLAGS, shell_PROPDESC_VIEW_FLAGS
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
targetos: Windows
req.typenames: PROPDESC_VIEW_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROPDESC_VIEW_FLAGS
 - propsys/PROPDESC_VIEW_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_VIEW_FLAGS
---

# PROPDESC_VIEW_FLAGS enumeration


## -description

These flags describe properties in property description list strings.

## -enum-fields

### -field PDVF_DEFAULT:0

Show this property by default.

### -field PDVF_CENTERALIGN:0x1

This property should be centered.

### -field PDVF_RIGHTALIGN:0x2

This property should be right aligned.

### -field PDVF_BEGINNEWGROUP:0x4

Show this property as the beginning of the next collection of properties in the view.

### -field PDVF_FILLAREA:0x8

Fill the remainder of the view area with the content of this property.

### -field PDVF_SORTDESCENDING:0x10

Sort this property in reverse (descending) order. Applies to a property in a list of sorted properties.

### -field PDVF_SHOWONLYIFPRESENT:0x20

Show this property only if it is present.

### -field PDVF_SHOWBYDEFAULT:0x40

This property should be shown by default in a view (where applicable).

### -field PDVF_SHOWINPRIMARYLIST:0x80

This property should be shown by default in the primary column selection UI.

### -field PDVF_SHOWINSECONDARYLIST:0x100

This property should be shown by default in the secondary column selection UI.

### -field PDVF_HIDELABEL:0x200

Hide the label of this property if the view normally shows the label.

### -field PDVF_HIDDEN:0x800

This property should not be displayed as a column in the UI.

### -field PDVF_CANWRAP:0x1000

This property can be wrapped to the next row.

### -field PDVF_MASK_ALL:0x1bff

A mask used to retrieve all flags.

## -remarks

These values are defined in propsys.h and propsys.idl.

