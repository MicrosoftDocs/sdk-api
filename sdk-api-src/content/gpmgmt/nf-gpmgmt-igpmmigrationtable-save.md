---
UID: NF:gpmgmt.IGPMMigrationTable.Save
title: IGPMMigrationTable::Save (gpmgmt.h)
description: Saves the migration table currently in memory in a specified location.
helpviewer_keywords: ["GPMMigrationTable class [GPMC]","Save method","IGPMMigrationTable interface [GPMC]","Save method","IGPMMigrationTable.Save","IGPMMigrationTable::Save","Save","Save method [GPMC]","Save method [GPMC]","GPMMigrationTable class","Save method [GPMC]","IGPMMigrationTable interface","gpmc.igpmmigrationtable_save","gpmgmt/IGPMMigrationTable::Save"]
old-location: gpmc\igpmmigrationtable_save.htm
tech.root: gpmc
ms.assetid: ce33306a-c72f-4231-a19c-eb733d87b361
ms.date: 12/05/2018
ms.keywords: GPMMigrationTable class [GPMC],Save method, IGPMMigrationTable interface [GPMC],Save method, IGPMMigrationTable.Save, IGPMMigrationTable::Save, Save, Save method [GPMC], Save method [GPMC],GPMMigrationTable class, Save method [GPMC],IGPMMigrationTable interface, gpmc.igpmmigrationtable_save, gpmgmt/IGPMMigrationTable::Save
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMMigrationTable::Save
 - gpmgmt/IGPMMigrationTable::Save
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.Save
 - GPMMigrationTable.Save
---

# IGPMMigrationTable::Save


## -description

Saves the migration table currently in memory in a specified location.

## -parameters

### -param bstrMigrationTablePath [in]

Path to file location where the migration table currently in memory is to be saved.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>