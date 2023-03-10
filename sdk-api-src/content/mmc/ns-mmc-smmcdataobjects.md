---
UID: NS:mmc._SMMCDataObjects
title: SMMCDataObjects (mmc.h)
description: The SMMCDataObjects structure defines the format of the data for the CCF_MULTI_SELECT_SNAPINS clipboard format.
helpviewer_keywords: ["SMMCDataObjects","SMMCDataObjects structure [MMC]","_slate_smmcdataobjects","mmc.smmcdataobjects","mmc/SMMCDataObjects"]
old-location: mmc\smmcdataobjects.htm
tech.root: mmc
ms.assetid: 4bbfc32e-b70b-4c47-a7b5-6ec2692d1df4
ms.date: 12/05/2018
ms.keywords: SMMCDataObjects, SMMCDataObjects structure [MMC], _slate_smmcdataobjects, mmc.smmcdataobjects, mmc/SMMCDataObjects
req.header: mmc.h
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
req.typenames: SMMCDataObjects
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SMMCDataObjects
 - mmc/_SMMCDataObjects
 - SMMCDataObjects
 - mmc/SMMCDataObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SMMCDataObjects
---

# SMMCDataObjects structure


## -description

The 
<b>SMMCDataObjects</b> structure defines the format of the data for the 
<a href="/previous-versions/windows/desktop/mmc/ccf-multi-select-snapins">CCF_MULTI_SELECT_SNAPINS</a> clipboard format. The structure contains the array of pointers to the multiselection data object of each snap-in represented in the set of selected items in the result pane.

## -struct-fields

### -field count

The number of snap-ins whose items are selected in the result pane.

### -field lpDataObject

Array of pointers to the multiselection data objects for each snap-in selected in the result pane.

## -remarks

Each data object consists of the node types associated with a given snap-in. Data objects are passed using 
<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>.

The multiselection data objects hold a list that contains each node type represented in the set of selected items for that particular snap-in in the result pane. The list of node types from a particular multiselection data object can be retrieved as an array of node type GUIDs by calling <b>IDataObject::GetData</b> on that data object with the 
<a href="/previous-versions/windows/desktop/mmc/ccf-object-types-in-multi-select">CCF_OBJECT_TYPES_IN_MULTI_SELECT</a> clipboard format.

Each multiselection data object also holds a list that contains the selected items owned by a particular snap-in. Each snap-in is responsible for defining the format and method of retrieval of the list of its selected items.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-multi-select-snapins">CCF_MULTI_SELECT_SNAPINS</a>



<a href="/previous-versions/windows/desktop/mmc/multiselection">Multiselection</a>



<a href="/windows/desktop/api/mmc/ns-mmc-smmcobjecttypes">SMMCObjectTypes</a>