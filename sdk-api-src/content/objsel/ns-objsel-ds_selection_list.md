---
UID: NS:objsel._DS_SELECTION_LIST
title: DS_SELECTION_LIST (objsel.h)
description: The DS_SELECTION_LIST structure contains data about the objects the user selected from an object picker dialog box.
helpviewer_keywords: ["*PDS_SELECTION_LIST","DS_SELECTION_LIST","DS_SELECTION_LIST structure [Active Directory]","PDS_SELECTION_LIST","PDS_SELECTION_LIST structure pointer [Active Directory]","_glines_ds_selection_list","ad.ds__selection__list","ad.ds_selection_list","objsel/DS_SELECTION_LIST","objsel/PDS_SELECTION_LIST"]
old-location: ad\ds_selection_list.htm
tech.root: ad
ms.assetid: 15493b8c-014e-4e69-9e67-40b24d44606d
ms.date: 12/05/2018
ms.keywords: '*PDS_SELECTION_LIST, DS_SELECTION_LIST, DS_SELECTION_LIST structure [Active Directory], PDS_SELECTION_LIST, PDS_SELECTION_LIST structure pointer [Active Directory], _glines_ds_selection_list, ad.ds__selection__list, ad.ds_selection_list, objsel/DS_SELECTION_LIST, objsel/PDS_SELECTION_LIST'
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DS_SELECTION_LIST, *PDS_SELECTION_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_SELECTION_LIST
 - objsel/_DS_SELECTION_LIST
 - PDS_SELECTION_LIST
 - objsel/PDS_SELECTION_LIST
 - DS_SELECTION_LIST
 - objsel/DS_SELECTION_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objsel.h
api_name:
 - DS_SELECTION_LIST
---

# DS_SELECTION_LIST structure


## -description

The <b>DS_SELECTION_LIST</b> structure contains data about the objects the user selected from an object picker dialog box. This structure is supplied by the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface supplied by the <a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-invokedialog">IDsObjectPicker::InvokeDialog</a> method in the <a href="/windows/desktop/AD/cfstr-dsop-ds-selection-list">CFSTR_DSOP_DS_SELECTION_LIST</a> data format.

## -struct-fields

### -field cItems

Contains the number of elements in the <b>aDsSelection</b> array.

### -field cFetchedAttributes

Contains the number of elements returned in the <b>pvarFetchedAttributes</b> member of each 
<a href="/windows/desktop/api/objsel/ns-objsel-ds_selection">DS_SELECTION</a> structure.

### -field aDsSelection

Contains an array of <a href="/windows/desktop/api/objsel/ns-objsel-ds_selection">DS_SELECTION</a> structures, one for each object selected by the user. The <b>cItems</b> member indicates the number of elements in this array.

## -see-also

<a href="/windows/desktop/AD/cfstr-dsop-ds-selection-list">CFSTR_DSOP_DS_SELECTION_LIST</a>



<a href="/windows/desktop/api/objsel/ns-objsel-ds_selection">DS_SELECTION</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-invokedialog">IDsObjectPicker::InvokeDialog</a>