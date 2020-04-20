---
UID: NE:mmc._DATA_OBJECT_TYPES
title: DATA_OBJECT_TYPES (mmc.h)
description: The DATA_OBJECT_TYPES enumeration is used by the type parameter of IComponentData::QueryDataObject and IComponent::QueryDataObject to obtain context information about a specified cookie.helpviewer_keywords: ["CCT_RESULT","CCT_SCOPE","CCT_SNAPIN_MANAGER","CCT_UNINITIALIZED","DATA_OBJECT_TYPES","DATA_OBJECT_TYPES enumeration [MMC]","_slate_data_object_types","mmc.data_object_types","mmc/CCT_RESULT","mmc/CCT_SCOPE","mmc/CCT_SNAPIN_MANAGER","mmc/CCT_UNINITIALIZED","mmc/DATA_OBJECT_TYPES"]
old-location: mmc\data_object_types.htm
tech.root: mmc
ms.assetid: 6f1cb622-b066-4208-9e25-cdd7e9c4dcd2
ms.date: 12/05/2018
ms.keywords: CCT_RESULT, CCT_SCOPE, CCT_SNAPIN_MANAGER, CCT_UNINITIALIZED, DATA_OBJECT_TYPES, DATA_OBJECT_TYPES enumeration [MMC], _slate_data_object_types, mmc.data_object_types, mmc/CCT_RESULT, mmc/CCT_SCOPE, mmc/CCT_SNAPIN_MANAGER, mmc/CCT_UNINITIALIZED, mmc/DATA_OBJECT_TYPES
f1_keywords:
- mmc/DATA_OBJECT_TYPES
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mmc.h
api_name:
- DATA_OBJECT_TYPES
targetos: Windows
req.typenames: DATA_OBJECT_TYPES
req.redist: 
ms.custom: 19H1
---

# DATA_OBJECT_TYPES enumeration


## -description


The 
<b>DATA_OBJECT_TYPES</b> enumeration is used by the <i>type</i> parameter of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">IComponentData::QueryDataObject</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a> to obtain context information about a specified cookie.


## -enum-fields




### -field CCT_SCOPE

Data object for scope pane context.


### -field CCT_RESULT

Data object for result pane context.


### -field CCT_SNAPIN_MANAGER

Data object for Snap-in Manager context.


### -field CCT_UNINITIALIZED

Data object has an invalid type.

