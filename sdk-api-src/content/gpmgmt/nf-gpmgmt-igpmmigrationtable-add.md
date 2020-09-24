---
UID: NF:gpmgmt.IGPMMigrationTable.Add
title: IGPMMigrationTable::Add (gpmgmt.h)
description: Adds entries from the IGPMGPO and IGPMBackup interfaces. The method updates any entries that are already present in the migration table.
helpviewer_keywords: ["Add","Add method [GPMC]","Add method [GPMC]","GPMMigrationTable class","Add method [GPMC]","IGPMMigrationTable interface","GPMMigrationTable class [GPMC]","Add method","GPM_PROCESS_SECURITY","IGPMMigrationTable interface [GPMC]","Add method","IGPMMigrationTable.Add","IGPMMigrationTable::Add","gpmc.igpmmigrationtable_add","gpmgmt/IGPMMigrationTable::Add"]
old-location: gpmc\igpmmigrationtable_add.htm
tech.root: gpmc
ms.assetid: e7be82b5-acb5-4e08-9771-d2698df3d0df
ms.date: 12/05/2018
ms.keywords: Add, Add method [GPMC], Add method [GPMC],GPMMigrationTable class, Add method [GPMC],IGPMMigrationTable interface, GPMMigrationTable class [GPMC],Add method, GPM_PROCESS_SECURITY, IGPMMigrationTable interface [GPMC],Add method, IGPMMigrationTable.Add, IGPMMigrationTable::Add, gpmc.igpmmigrationtable_add, gpmgmt/IGPMMigrationTable::Add
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
 - IGPMMigrationTable::Add
 - gpmgmt/IGPMMigrationTable::Add
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
 - IGPMMigrationTable.Add
 - GPMMigrationTable.Add
---

## -description

Adds entries from the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> and <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interfaces. The method updates any entries that are already present in the migration table.

## -parameters

### -param lFlags [in]

This parameter must be one of the following values.

#### 0

Do not take security principals from the DACLs in the backup GPO or the live GPO.

#### GPM_PROCESS_SECURITY

Copy all the entries from the DACLs and settings.

### -param var [in]

Dispatch pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> or <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interface.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a>