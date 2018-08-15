---
UID: NE:mmc._DATA_OBJECT_TYPES
title: "_DATA_OBJECT_TYPES"
author: windows-sdk-content
description: The DATA_OBJECT_TYPES enumeration is used by the type parameter of IComponentData::QueryDataObject and IComponent::QueryDataObject to obtain context information about a specified cookie.
old-location: mmc\data_object_types.htm
old-project: MMC
ms.assetid: 6f1cb622-b066-4208-9e25-cdd7e9c4dcd2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CCT_RESULT, CCT_SCOPE, CCT_SNAPIN_MANAGER, CCT_UNINITIALIZED, DATA_OBJECT_TYPES, DATA_OBJECT_TYPES enumeration [MMC], _DATA_OBJECT_TYPES, _slate_data_object_types, mmc.data_object_types, mmc/CCT_RESULT, mmc/CCT_SCOPE, mmc/CCT_SNAPIN_MANAGER, mmc/CCT_UNINITIALIZED, mmc/DATA_OBJECT_TYPES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DATA_OBJECT_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - DATA_OBJECT_TYPES
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DATA_OBJECT_TYPES enumeration


## -description


The 
<b>DATA_OBJECT_TYPES</b> enumeration is used by the <i>type</i> parameter of 
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">IComponentData::QueryDataObject</a> and 
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a> to obtain context information about a specified cookie.


## -enum-fields




### -field CCT_SCOPE

Data object for scope pane context.


### -field CCT_RESULT

Data object for result pane context.


### -field CCT_SNAPIN_MANAGER

Data object for Snap-in Manager context.


### -field CCT_UNINITIALIZED

Data object has an invalid type.

