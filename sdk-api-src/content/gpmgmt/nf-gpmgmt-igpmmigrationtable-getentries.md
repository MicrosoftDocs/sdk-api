---
UID: NF:gpmgmt.IGPMMigrationTable.GetEntries
title: IGPMMigrationTable::GetEntries (gpmgmt.h)
description: Returns a IGPMMapEntryCollection interface.
helpviewer_keywords: ["GPMMigrationTable class [GPMC]","GetEntries method","GetEntries","GetEntries method [GPMC]","GetEntries method [GPMC]","GPMMigrationTable class","GetEntries method [GPMC]","IGPMMigrationTable interface","IGPMMigrationTable interface [GPMC]","GetEntries method","IGPMMigrationTable.GetEntries","IGPMMigrationTable::GetEntries","gpmc.igpmmigrationtable_getentries","gpmgmt/IGPMMigrationTable::GetEntries"]
old-location: gpmc\igpmmigrationtable_getentries.htm
tech.root: gpmc
ms.assetid: 5de22bba-10f9-49f7-83f3-053f5e58b66e
ms.date: 12/05/2018
ms.keywords: GPMMigrationTable class [GPMC],GetEntries method, GetEntries, GetEntries method [GPMC], GetEntries method [GPMC],GPMMigrationTable class, GetEntries method [GPMC],IGPMMigrationTable interface, IGPMMigrationTable interface [GPMC],GetEntries method, IGPMMigrationTable.GetEntries, IGPMMigrationTable::GetEntries, gpmc.igpmmigrationtable_getentries, gpmgmt/IGPMMigrationTable::GetEntries
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
 - IGPMMigrationTable::GetEntries
 - gpmgmt/IGPMMigrationTable::GetEntries
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
 - IGPMMigrationTable.GetEntries
 - GPMMigrationTable.GetEntries
---

# IGPMMigrationTable::GetEntries


## -description

Returns a <b>IGPMMapEntryCollection</b> interface.

## -parameters

### -param ppEntries [out]

The list of entries in the migration table.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentrycollection">GPMMapEntryCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentrycollection">GPMMapEntryCollection</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>