---
UID: NF:gpmgmt.IGPMMigrationTable.DeleteEntry
title: IGPMMigrationTable::DeleteEntry (gpmgmt.h)
description: Deletes an entry from the migration table.
helpviewer_keywords: ["DeleteEntry","DeleteEntry method [GPMC]","DeleteEntry method [GPMC]","GPMMigrationTable class","DeleteEntry method [GPMC]","IGPMMigrationTable interface","GPMMigrationTable class [GPMC]","DeleteEntry method","IGPMMigrationTable interface [GPMC]","DeleteEntry method","IGPMMigrationTable.DeleteEntry","IGPMMigrationTable::DeleteEntry","gpmc.igpmmigrationtable_deleteentry","gpmgmt/IGPMMigrationTable::DeleteEntry"]
old-location: gpmc\igpmmigrationtable_deleteentry.htm
tech.root: gpmc
ms.assetid: 712a6419-2f64-4657-993a-e7f6bfc1259e
ms.date: 12/05/2018
ms.keywords: DeleteEntry, DeleteEntry method [GPMC], DeleteEntry method [GPMC],GPMMigrationTable class, DeleteEntry method [GPMC],IGPMMigrationTable interface, GPMMigrationTable class [GPMC],DeleteEntry method, IGPMMigrationTable interface [GPMC],DeleteEntry method, IGPMMigrationTable.DeleteEntry, IGPMMigrationTable::DeleteEntry, gpmc.igpmmigrationtable_deleteentry, gpmgmt/IGPMMigrationTable::DeleteEntry
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
 - IGPMMigrationTable::DeleteEntry
 - gpmgmt/IGPMMigrationTable::DeleteEntry
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
 - IGPMMigrationTable.DeleteEntry
 - GPMMigrationTable.DeleteEntry
---

# IGPMMigrationTable::DeleteEntry


## -description

Deletes an entry from the migration table.

## -parameters

### -param bstrSource [in]

Source field of the entry to delete. Use null-terminated string.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a>