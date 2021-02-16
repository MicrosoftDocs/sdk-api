---
UID: NF:gpmgmt.IGPM.CreateMigrationTable
title: IGPM::CreateMigrationTable (gpmgmt.h)
description: Creates an empty migration table.
helpviewer_keywords: ["CreateMigrationTable","CreateMigrationTable method [GPMC]","CreateMigrationTable method [GPMC]","GPM class","CreateMigrationTable method [GPMC]","IGPM interface","GPM class [GPMC]","CreateMigrationTable method","IGPM interface [GPMC]","CreateMigrationTable method","IGPM.CreateMigrationTable","IGPM::CreateMigrationTable","gpmc.igpm_createmigrationtable","gpmgmt/IGPM::CreateMigrationTable"]
old-location: gpmc\igpm_createmigrationtable.htm
tech.root: gpmc
ms.assetid: ae9ea50f-d652-4d7a-aac5-5b9ef27b99e0
ms.date: 12/05/2018
ms.keywords: CreateMigrationTable, CreateMigrationTable method [GPMC], CreateMigrationTable method [GPMC],GPM class, CreateMigrationTable method [GPMC],IGPM interface, GPM class [GPMC],CreateMigrationTable method, IGPM interface [GPMC],CreateMigrationTable method, IGPM.CreateMigrationTable, IGPM::CreateMigrationTable, gpmc.igpm_createmigrationtable, gpmgmt/IGPM::CreateMigrationTable
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
 - IGPM::CreateMigrationTable
 - gpmgmt/IGPM::CreateMigrationTable
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
 - IGPM.CreateMigrationTable
 - GPM.CreateMigrationTable
---

# IGPM::CreateMigrationTable


## -description

Creates an empty migration table.

## -parameters

### -param ppMigrationTable [out]

Receives the created migration table that contains no entries. See <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a>.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMigrationTable</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMigrationTable</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a>