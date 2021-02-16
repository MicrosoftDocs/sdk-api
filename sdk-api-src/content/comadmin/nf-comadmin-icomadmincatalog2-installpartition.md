---
UID: NF:comadmin.ICOMAdminCatalog2.InstallPartition
title: ICOMAdminCatalog2::InstallPartition (comadmin.h)
description: Imports a partition from a file.
helpviewer_keywords: ["COMAdminInstallForceOverwriteOfFile","COMAdminInstallNoUsers","COMAdminInstallUsers","ICOMAdminCatalog2 interface [COM+]","InstallPartition method","ICOMAdminCatalog2.InstallPartition","ICOMAdminCatalog2::InstallPartition","InstallPartition","InstallPartition method [COM+]","InstallPartition method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_InstallPartition","comadmin/ICOMAdminCatalog2::InstallPartition","cos.icomadmincatalog2_installpartition"]
old-location: cos\icomadmincatalog2_installpartition.htm
tech.root: cos
ms.assetid: e1f54a6a-9b90-4e9e-b94c-46f6c9b683a3
ms.date: 12/05/2018
ms.keywords: COMAdminInstallForceOverwriteOfFile, COMAdminInstallNoUsers, COMAdminInstallUsers, ICOMAdminCatalog2 interface [COM+],InstallPartition method, ICOMAdminCatalog2.InstallPartition, ICOMAdminCatalog2::InstallPartition, InstallPartition, InstallPartition method [COM+], InstallPartition method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_InstallPartition, comadmin/ICOMAdminCatalog2::InstallPartition, cos.icomadmincatalog2_installpartition
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICOMAdminCatalog2::InstallPartition
 - comadmin/ICOMAdminCatalog2::InstallPartition
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
 - ICOMAdminCatalog2.InstallPartition
---

# ICOMAdminCatalog2::InstallPartition


## -description

Imports a partition from a file.

## -parameters

### -param bstrFileName [in]

The file from which the partition is to be imported.

### -param bstrDestDirectory [in]

The path to the directory in which to install the partition components.

### -param lOptions [in]

The install options. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallNoUsers"></a><a id="comadmininstallnousers"></a><a id="COMADMININSTALLNOUSERS"></a><dl>
<dt><b>COMAdminInstallNoUsers</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not install users saved in the partition (default).

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallUsers"></a><a id="comadmininstallusers"></a><a id="COMADMININSTALLUSERS"></a><dl>
<dt><b>COMAdminInstallUsers</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Install users saved in the partition.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallForceOverwriteOfFile"></a><a id="comadmininstallforceoverwriteoffile"></a><a id="COMADMININSTALLFORCEOVERWRITEOFFILE"></a><dl>
<dt><b>COMAdminInstallForceOverwriteOfFile</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Overwrite existing files.

</td>
</tr>
</table>

### -param bstrUserID [in]

The user ID under which to install the partition.

### -param bstrPassword [in]

The password for the specified user.

### -param bstrRSN [in]

The name of a remote server to use as a proxy.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>