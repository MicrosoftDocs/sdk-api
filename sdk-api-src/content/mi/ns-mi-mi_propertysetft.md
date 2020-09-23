---
UID: NS:mi._MI_PropertySetFT
title: MI_PropertySetFT (mi.h)
description: A support structure used in the MI_PropertySet structure. Use the functions with the name prefix &quot;MI_PropertySet_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_PropertySetFT","MI_PropertySetFT structure [Windows Management Infrastructure (MI)]","mi/MI_PropertySetFT","wmi_v2.mi_propertysetft"]
old-location: wmi_v2\mi_propertysetft.htm
tech.root: wmi_v2
ms.assetid: d71c0378-0b97-44ea-9f42-e533b93f195e
ms.date: 12/05/2018
ms.keywords: MI_PropertySetFT, MI_PropertySetFT structure [Windows Management Infrastructure (MI)], mi/MI_PropertySetFT, wmi_v2.mi_propertysetft
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
targetos: Windows
req.typenames: MI_PropertySetFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_PropertySetFT
 - mi/_MI_PropertySetFT
 - MI_PropertySetFT
 - mi/MI_PropertySetFT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_PropertySetFT
---

## -description

A support structure used in the 
     <a href="/windows/desktop/api/mi/ns-mi-mi_propertyset">MI_PropertySet</a> structure. Use the functions with the 
     name prefix "MI_PropertySet_" to manipulate these structures.

## -struct-fields

### -field AddElement

Adds a name to the property list. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_addelement">MI_PropertySet_AddElement</a>.

### -field Clear

Removes all names from the property list. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_clear">MI_PropertySet_Clear</a>.

### -field Clone

Creates a copy of the specified property set on the heap. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_clone">MI_PropertySet_Clone</a>.

### -field ContainsElement

Determines whether the property list contains the specified property. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_containselement">MI_PropertySet_ContainsElement</a>.

### -field Delete

Deletes the specified property list that was constructed on the heap. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_delete">MI_PropertySet_Delete</a>.

### -field Destruct

Deletes the specified property list that was constructed on the stack. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_destruct">MI_PropertySet_Destruct</a>.

### -field GetElementAt

Gets the element of a property set at the specified index. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_getelementat">MI_PropertySet_GetElementAt</a>.

### -field GetElementCount

Gets the number of elements in the specified property set. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_propertyset_getelementcount">MI_PropertySet_GetElementCount</a>.
       