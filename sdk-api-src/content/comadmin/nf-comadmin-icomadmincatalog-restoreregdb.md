---
UID: NF:comadmin.ICOMAdminCatalog.RestoreREGDB
title: ICOMAdminCatalog::RestoreREGDB
author: windows-sdk-content
description: Restores the COM+ class registration database (RegDB) from the specified file. For this to take effect, a system reboot is required.
old-location: cos\icomadmincatalog_restoreregdb.htm
old-project: cossdk
ms.assetid: 7cb2201c-601c-4add-8608-3f98ef92c26d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ICOMAdminCatalog interface [COM+],RestoreREGDB method, ICOMAdminCatalog.RestoreREGDB, ICOMAdminCatalog::RestoreREGDB, RestoreREGDB, RestoreREGDB method [COM+], RestoreREGDB method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_RestoreREGDB, comadmin/ICOMAdminCatalog::RestoreREGDB, cos.icomadmincatalog_restoreregdb
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.RestoreREGDB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

