---
UID: NF:comadmin.ICOMAdminCatalog.RestoreREGDB
title: ICOMAdminCatalog::RestoreREGDB (comadmin.h)
description: Restores the COM+ class registration database (RegDB) from the specified file. For this to take effect, a system reboot is required.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","RestoreREGDB method","ICOMAdminCatalog.RestoreREGDB","ICOMAdminCatalog::RestoreREGDB","RestoreREGDB","RestoreREGDB method [COM+]","RestoreREGDB method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_RestoreREGDB","comadmin/ICOMAdminCatalog::RestoreREGDB","cos.icomadmincatalog_restoreregdb"]
old-location: cos\icomadmincatalog_restoreregdb.htm
tech.root: cos
ms.assetid: 7cb2201c-601c-4add-8608-3f98ef92c26d
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],RestoreREGDB method, ICOMAdminCatalog.RestoreREGDB, ICOMAdminCatalog::RestoreREGDB, RestoreREGDB, RestoreREGDB method [COM+], RestoreREGDB method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_RestoreREGDB, comadmin/ICOMAdminCatalog::RestoreREGDB, cos.icomadmincatalog_restoreregdb
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
 - ICOMAdminCatalog::RestoreREGDB
 - comadmin/ICOMAdminCatalog::RestoreREGDB
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
 - ICOMAdminCatalog.RestoreREGDB
---

# ICOMAdminCatalog::RestoreREGDB


## -description

Restores the COM+ class registration database (RegDB) from the specified file. For this to take effect, a system reboot is required.

## -parameters

### -param bstrBackupFilePath [in]

The name of the file to which the database was backed up.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECTERRORS</b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>