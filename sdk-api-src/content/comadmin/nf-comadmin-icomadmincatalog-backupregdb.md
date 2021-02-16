---
UID: NF:comadmin.ICOMAdminCatalog.BackupREGDB
title: ICOMAdminCatalog::BackupREGDB (comadmin.h)
description: Backs up the COM+ class registration database to a specified file.
helpviewer_keywords: ["BackupREGDB","BackupREGDB method [COM+]","BackupREGDB method [COM+]","ICOMAdminCatalog interface","ICOMAdminCatalog interface [COM+]","BackupREGDB method","ICOMAdminCatalog.BackupREGDB","ICOMAdminCatalog::BackupREGDB","_cos_ICOMAdminCatalog_BackupREGDB","comadmin/ICOMAdminCatalog::BackupREGDB","cos.icomadmincatalog_backupregdb"]
old-location: cos\icomadmincatalog_backupregdb.htm
tech.root: cos
ms.assetid: dd350abd-3b59-4a5d-b2e4-1ddeec2b1953
ms.date: 12/05/2018
ms.keywords: BackupREGDB, BackupREGDB method [COM+], BackupREGDB method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],BackupREGDB method, ICOMAdminCatalog.BackupREGDB, ICOMAdminCatalog::BackupREGDB, _cos_ICOMAdminCatalog_BackupREGDB, comadmin/ICOMAdminCatalog::BackupREGDB, cos.icomadmincatalog_backupregdb
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog::BackupREGDB
 - comadmin/ICOMAdminCatalog::BackupREGDB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.BackupREGDB
---

# ICOMAdminCatalog::BackupREGDB


## -description

Backs up the COM+ class registration database to a specified file.

## -parameters

### -param bstrBackupFilePath [in]

The path for the file in which the registration database is to be backed up.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>