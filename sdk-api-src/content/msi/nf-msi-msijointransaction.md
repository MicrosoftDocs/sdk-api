---
UID: NF:msi.MsiJoinTransaction
title: MsiJoinTransaction function (msi.h)
description: The MsiJoinTransaction function requests that the Windows Installer make the current process the owner of the transaction installing the multiple-package installation.
helpviewer_keywords: ["MsiJoinTransaction","MsiJoinTransaction function [Setup API]","msi/MsiJoinTransaction","setup.msijointransaction"]
old-location: setup\msijointransaction.htm
tech.root: setup
ms.assetid: 222c37fd-1a77-4017-8e55-cbd844f375df
ms.date: 12/05/2018
ms.keywords: MsiJoinTransaction, MsiJoinTransaction function [Setup API], msi/MsiJoinTransaction, setup.msijointransaction
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
 - MsiJoinTransaction
 - msi/MsiJoinTransaction
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
 - MsiJoinTransaction
---

# MsiJoinTransaction function


## -description

The <b>MsiJoinTransaction</b> function requests that the Windows Installer make the current process the owner of the <a href="/windows/desktop/Msi/t-gly">transaction</a> installing the multiple-package installation. 

<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-0">Windows Installer 4.0 and earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 4.5.

## -parameters

### -param hTransactionHandle [in]

The transaction ID, which identifies the transaction and is the identifier returned by the <a href="/windows/desktop/api/msi/nf-msi-msibegintransactiona">MsiBeginTransaction</a> function.

### -param dwTransactionAttributes [in]

Attributes of the multiple-package installation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
When 0 or no value is set, Windows Installer closes the UI from the previous installation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTION_CHAIN_EMBEDDEDUI</dt>
</dl>
</td>
<td width="60%">
Set this attribute to request that the Windows Installer not shutdown the embedded UI until the transaction is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTION_JOIN_EXISTING_EMBEDDEDUI</dt>
</dl>
</td>
<td width="60%">
Set this attribute to request that the Windows Installer transfer the embedded UI from the original installation. If the original installation has no embedded UI, setting this attribute does nothing.

</td>
</tr>
</table>

### -param phChangeOfOwnerEvent [out]

This parameter returns a handle to an event that  is set when the <b>MsiJoinTransaction</b> function changes the owner of the transaction to a new owner. The current owner can use this to determine when ownership of the transaction has changed. Leaving a transaction without an owner will roll back the transaction.

## -returns

The <b>MsiJoinTransaction</b> function can return the following values.
					

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
The user that owns the transaction and the user that joins the transaction are not the same. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter that is not valid is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The owner cannot be changed while an active installation is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The transaction ID provided is not valid.

</td>
</tr>
</table>

## -remarks

Because a transaction can be owned by no more than one process at a time, the functions authored into the <a href="/windows/desktop/Msi/msiembeddedchainer-table">MsiEmbeddedChainer table</a> can use <b>MsiJoinTransaction</b> to request ownership of the transaction before using the Windows Installer API to configure or install an application. The installer verifies that there is no installation in progress. The installer verifies that the process requesting ownership and the process that currently owns the transaction share a parent process in the same process tree.  If the function succeeds, the process that calls <b>MsiJoinTransaction</b> becomes the current owner of the transaction.

<b>MsiJoinTransaction</b> sets the internal UI of the new installation to the UI level of the original installation. After the new installation owns the transaction, it can call <a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a> to change the UI level.  This enables the new installation to run at a higher UI level than the original installation.

## -see-also

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple Package Installations</a>