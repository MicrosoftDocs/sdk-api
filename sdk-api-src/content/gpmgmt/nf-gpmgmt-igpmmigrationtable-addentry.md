---
UID: NF:gpmgmt.IGPMMigrationTable.AddEntry
title: IGPMMigrationTable::AddEntry (gpmgmt.h)
description: Creates an entry in the migration table. The method updates an existing entry.
helpviewer_keywords: ["AddEntry","AddEntry method [GPMC]","AddEntry method [GPMC]","GPMMigrationTable class","AddEntry method [GPMC]","IGPMMigrationTable interface","GPMMigrationTable class [GPMC]","AddEntry method","IGPMMigrationTable interface [GPMC]","AddEntry method","IGPMMigrationTable.AddEntry","IGPMMigrationTable::AddEntry","gpmc.igpmmigrationtable_addentry","gpmgmt/IGPMMigrationTable::AddEntry","typeComputer","typeGlobalGroup","typeLocalGroup","typeUNCPath","typeUniversalGroup","typeUnknown","typeUser"]
old-location: gpmc\igpmmigrationtable_addentry.htm
tech.root: gpmc
ms.assetid: 2e6f6b81-b01c-4d46-9b7b-3265580f112a
ms.date: 12/05/2018
ms.keywords: AddEntry, AddEntry method [GPMC], AddEntry method [GPMC],GPMMigrationTable class, AddEntry method [GPMC],IGPMMigrationTable interface, GPMMigrationTable class [GPMC],AddEntry method, IGPMMigrationTable interface [GPMC],AddEntry method, IGPMMigrationTable.AddEntry, IGPMMigrationTable::AddEntry, gpmc.igpmmigrationtable_addentry, gpmgmt/IGPMMigrationTable::AddEntry, typeComputer, typeGlobalGroup, typeLocalGroup, typeUNCPath, typeUniversalGroup, typeUnknown, typeUser
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
 - IGPMMigrationTable::AddEntry
 - gpmgmt/IGPMMigrationTable::AddEntry
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
 - IGPMMigrationTable.AddEntry
 - GPMMigrationTable.AddEntry
---

## -description

Creates an entry in the migration table. The method updates an existing entry.

## -parameters

### -param bstrSource [in]

Source field of the entry. This parameter cannot be null.

### -param gpmEntryType [in]

This parameter must be one of the following values.

#### typeUser

This value equals 0 (zero). Creates a User entry in the migration table.

#### typeComputer

Creates an entry for a User.

#### typeLocalGroup

Creates an entry for a LocalGroup.

#### typeGlobalGroup

Creates an entry for a GlobalGroup.

#### typeUniversalGroup

Creates an entry for a UniversalGroup.

#### typeUNCPath

Creates an entry for a UNCPath.

#### typeUnknown

Creates an entry for an unknown.

### -param pvarDestination [in, optional]

A pointer to a <b>VARIANT</b> structure. You can use the <b>DestinationOptions</b>: <b>opDestinationSameAsSource</b>, <b>opDestinationNone</b>, or <b>opDestinationByRelativeName</b> by passing in a <i>pvarDestination</i> with a <b>vt</b> member of VT_I4. To explicitly pass in the destination, pass in a <i>pvarDestination</i> with a <b>vt</b> member of VT_BSTR, and this sets the <b>DestinationOptions</b> to <b>opDestinationSet</b>. If you pass in null, <b>AddEntry</b> uses the default value for the destination option, <b>opDestinationSameAsSource</b>.

### -param ppEntry [out]

The new entry.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>
