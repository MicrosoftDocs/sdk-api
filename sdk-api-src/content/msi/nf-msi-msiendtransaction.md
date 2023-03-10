---
UID: NF:msi.MsiEndTransaction
title: MsiEndTransaction function (msi.h)
description: The MsiEndTransaction function can commit or roll back all the installations belonging to the transaction opened by the MsiBeginTransaction function.
helpviewer_keywords: ["MsiEndTransaction","MsiEndTransaction function [Setup API]","msi/MsiEndTransaction","setup.msiendtransaction"]
old-location: setup\msiendtransaction.htm
tech.root: setup
ms.assetid: 70912430-63d7-4087-858c-fb13f47008e2
ms.date: 12/05/2018
ms.keywords: MsiEndTransaction, MsiEndTransaction function [Setup API], msi/MsiEndTransaction, setup.msiendtransaction
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiEndTransaction
 - msi/MsiEndTransaction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiEndTransaction
---

# MsiEndTransaction function


## -description

The  <b>MsiEndTransaction</b> function can commit or roll back all the installations belonging to the transaction opened by the <a href="/windows/desktop/api/msi/nf-msi-msibegintransactiona">MsiBeginTransaction</a> function. This function should be called by the current owner of the transaction. 

<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-0">Windows Installer 4.0 and earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 4.5.

## -parameters

### -param dwTransactionState [in]

The value of this parameter determines whether the installer commits or rolls back all the installations belonging to the transaction. The value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTIONSTATE_ROLLBACK</dt>
</dl>
</td>
<td width="60%">
Performs a <a href="/windows/desktop/Msi/rollback-installation">Rollback Installation</a> to undo changes to the system belonging to the transaction opened by the <a href="/windows/desktop/api/msi/nf-msi-msibegintransactiona">MsiBeginTransaction</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTIONSTATE_COMMIT</dt>
</dl>
</td>
<td width="60%">
Commits all changes to the system belonging to the transaction. Runs any <a href="/windows/desktop/Msi/commit-custom-actions">Commit Custom Actions</a> and commits to the system any changes to Win32 or common language runtime assemblies. Deletes the rollback script, and after using this option, the transaction's changes can no longer be undone with a  <a href="/windows/desktop/Msi/rollback-installation">Rollback Installation</a>.  

</td>
</tr>
</table>

## -returns

The <b>MsiEndTransaction</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
A transaction can be ended only by the current owner.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction could not be completed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction is still in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ROLLBACK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
An installation belonging to the transaction did not complete. During the installation, the <a href="/windows/desktop/Msi/disablerollback-action">DisableRollback</a> action disabled <a href="/windows/desktop/Msi/rollback-installation">rollback installations</a> of the package. The installer rolls back the installation up to the point where rollback was disabled, and the function returns this error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple Package Installations</a>