---
UID: NF:gpmgmt.IGPMMigrationTable.UpdateDestination
title: IGPMMigrationTable::UpdateDestination (gpmgmt.h)
description: Updates the destination field of an entry in a migration table. You can specify the destination option and the destination.
helpviewer_keywords: ["GPMigrationTable class [GPMC]","UpdateDestination method","IGPMMigrationTable interface [GPMC]","UpdateDestination method","IGPMMigrationTable.UpdateDestination","IGPMMigrationTable::UpdateDestination","UpdateDestination","UpdateDestination method [GPMC]","UpdateDestination method [GPMC]","GPMigrationTable class","UpdateDestination method [GPMC]","IGPMMigrationTable interface","gpmc.igpmmigrationtable_updatedestination","gpmgmt/IGPMMigrationTable::UpdateDestination"]
old-location: gpmc\igpmmigrationtable_updatedestination.htm
tech.root: gpmc
ms.assetid: c47ad9d7-cf04-4ab4-9c44-78a5e54fc04e
ms.date: 12/05/2018
ms.keywords: GPMigrationTable class [GPMC],UpdateDestination method, IGPMMigrationTable interface [GPMC],UpdateDestination method, IGPMMigrationTable.UpdateDestination, IGPMMigrationTable::UpdateDestination, UpdateDestination, UpdateDestination method [GPMC], UpdateDestination method [GPMC],GPMigrationTable class, UpdateDestination method [GPMC],IGPMMigrationTable interface, gpmc.igpmmigrationtable_updatedestination, gpmgmt/IGPMMigrationTable::UpdateDestination
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
 - IGPMMigrationTable::UpdateDestination
 - gpmgmt/IGPMMigrationTable::UpdateDestination
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
 - IGPMMigrationTable.UpdateDestination
 - GPMigrationTable.UpdateDestination
---

## -description

Updates the destination field of an entry in a migration table. You can specify the destination option and the destination.

## -parameters

### -param bstrSource [in]

The source field of the migration table which is to be updated.

### -param pvarDestination [in, optional]

A pointer to a <b>VARIANT</b> structure.  You can  use the DestinationOptions: opDestinationSameAsSource, opDestinationNone, or opDestinationByRelativeName by passing  in a <i>pvarDestination</i> with a <b>vt</b> member of VT_I4. To explicitly pass in the destination,  pass in a <i>pvarDestination</i> with a <b>vt</b> member of VT_BSTR, and this will set the DestinationOption to opDestinationSet. If you pass in null, UpdateDestination uses the default value for the destination option, opDestinationSameAsSource.

### -param ppEntry [out]

The updated entry.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>