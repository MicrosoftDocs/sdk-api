---
UID: NF:msi.MsiBeginTransactionW
title: MsiBeginTransactionW function (msi.h)
description: The MsiBeginTransaction function starts transaction processing of a multiple-package installation and returns an identifier for the transaction. (Unicode)
helpviewer_keywords: ["MsiBeginTransaction", "MsiBeginTransaction function [Setup API]", "MsiBeginTransactionW", "msi/MsiBeginTransaction", "msi/MsiBeginTransactionW", "setup.msibegintransaction"]
old-location: setup\msibegintransaction.htm
tech.root: setup
ms.assetid: 05904e58-b24d-4d2c-8b59-a66ad71b494a
ms.date: 12/05/2018
ms.keywords: MsiBeginTransaction, MsiBeginTransaction function [Setup API], MsiBeginTransactionA, MsiBeginTransactionW, msi/MsiBeginTransaction, msi/MsiBeginTransactionA, msi/MsiBeginTransactionW, setup.msibegintransaction
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiBeginTransactionW (Unicode) and MsiBeginTransactionA (ANSI)
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
 - MsiBeginTransactionW
 - msi/MsiBeginTransactionW
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
 - MsiBeginTransaction
 - MsiBeginTransactionA
 - MsiBeginTransactionW
---

# MsiBeginTransactionW function


## -description

The  <b>MsiBeginTransaction</b> function starts <a href="/windows/desktop/Msi/t-gly">transaction processing</a> of a multiple-package installation and returns an identifier for the transaction. The  <a href="/windows/desktop/api/msi/nf-msi-msiendtransaction">MsiEndTransaction</a> function ends  the transaction.

<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-0">Windows Installer 4.0 and earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 4.5.

## -parameters

### -param szName [in]

Name of the multiple-package installation.

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
When 0 or no value is set it Windows Installer closes the UI from the previous installation.

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
</table>

### -param phTransactionHandle [out]

Transaction ID is a <b>MSIHANDLE</b> value that identifies the transaction. Only one process can own a transaction at a  time.

### -param phChangeOfOwnerEvent [out]

This parameter returns a handle to an event that  is set when the <a href="/windows/desktop/api/msi/nf-msi-msijointransaction">MsiJoinTransaction</a> function changes the owner of the transaction to a new owner. The current owner can use this to determine when ownership of the transaction has changed. Leaving a transaction without an owner will roll back the transaction.

## -returns

The <b>MsiBeginTransaction</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation service could not be accessed. This function requires the Windows Installer service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
Only one transaction can be open on a system at a time. The function returns this error if  called while another transaction is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ROLLBACK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Msi/rollback-installation">Rollback Installations</a> have been disabled by the <a href="/windows/desktop/Msi/-disablerollback">DISABLEROLLBACK</a> property or <a href="/windows/desktop/Msi/disablerollback">DisableRollback</a> policy.     

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/multiple-package-installations">Multiple Package Installations</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiBeginTransaction as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
