---
UID: NF:msiquery.MsiGetMode
title: MsiGetMode function (msiquery.h)
description: The MsiGetMode function is used to determine whether the installer is currently running in a specified mode, as listed in the table.
helpviewer_keywords: ["MSIRUNMODE_ADMIN","MSIRUNMODE_ADVERTISE","MSIRUNMODE_CABINET","MSIRUNMODE_COMMIT","MSIRUNMODE_LOGENABLED","MSIRUNMODE_MAINTENANCE","MSIRUNMODE_OPERATIONS","MSIRUNMODE_REBOOTATEND","MSIRUNMODE_REBOOTNOW","MSIRUNMODE_RESERVED11","MSIRUNMODE_RESERVED14","MSIRUNMODE_RESERVED15","MSIRUNMODE_ROLLBACK","MSIRUNMODE_ROLLBACKENABLED","MSIRUNMODE_SCHEDULED","MSIRUNMODE_SOURCESHORTNAMES","MSIRUNMODE_TARGETSHORTNAMES","MSIRUNMODE_WINDOWS9X","MSIRUNMODE_ZAWENABLED","MsiGetMode","MsiGetMode function","_msi_msigetmode","msiquery/MsiGetMode","setup.msigetmode"]
old-location: setup\msigetmode.htm
tech.root: setup
ms.assetid: 45827df5-3f3f-4fb9-bdfe-38dc78a45321
ms.date: 12/05/2018
ms.keywords: MSIRUNMODE_ADMIN, MSIRUNMODE_ADVERTISE, MSIRUNMODE_CABINET, MSIRUNMODE_COMMIT, MSIRUNMODE_LOGENABLED, MSIRUNMODE_MAINTENANCE, MSIRUNMODE_OPERATIONS, MSIRUNMODE_REBOOTATEND, MSIRUNMODE_REBOOTNOW, MSIRUNMODE_RESERVED11, MSIRUNMODE_RESERVED14, MSIRUNMODE_RESERVED15, MSIRUNMODE_ROLLBACK, MSIRUNMODE_ROLLBACKENABLED, MSIRUNMODE_SCHEDULED, MSIRUNMODE_SOURCESHORTNAMES, MSIRUNMODE_TARGETSHORTNAMES, MSIRUNMODE_WINDOWS9X, MSIRUNMODE_ZAWENABLED, MsiGetMode, MsiGetMode function, _msi_msigetmode, msiquery/MsiGetMode, setup.msigetmode
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
 - MsiGetMode
 - msiquery/MsiGetMode
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
 - MsiGetMode
---

# MsiGetMode function


## -description

The 
<b>MsiGetMode</b> function is used to determine whether the installer is currently running in a specified mode, as listed in the table. The function returns a Boolean value of <b>TRUE</b> or <b>FALSE</b>, indicating whether the specific property passed into the function is currently set (<b>TRUE</b>) or not set (<b>FALSE</b>).

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param eRunMode [in]

Specifies the run mode. This parameter must have one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_ADMIN"></a><a id="msirunmode_admin"></a><dl>
<dt><b>MSIRUNMODE_ADMIN</b></dt>
</dl>
</td>
<td width="60%">
The administrative mode is installing, or the product is installing.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_ADVERTISE"></a><a id="msirunmode_advertise"></a><dl>
<dt><b>MSIRUNMODE_ADVERTISE</b></dt>
</dl>
</td>
<td width="60%">
The advertisements are installing or the product is installing or updating.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_MAINTENANCE"></a><a id="msirunmode_maintenance"></a><dl>
<dt><b>MSIRUNMODE_MAINTENANCE</b></dt>
</dl>
</td>
<td width="60%">
An existing installation is being modified or there is a new installation.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_ROLLBACKENABLED"></a><a id="msirunmode_rollbackenabled"></a><dl>
<dt><b>MSIRUNMODE_ROLLBACKENABLED</b></dt>
</dl>
</td>
<td width="60%">
Rollback is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_LOGENABLED"></a><a id="msirunmode_logenabled"></a><dl>
<dt><b>MSIRUNMODE_LOGENABLED</b></dt>
</dl>
</td>
<td width="60%">
The log file is active. It was enabled prior to the installation session.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_OPERATIONS"></a><a id="msirunmode_operations"></a><dl>
<dt><b>MSIRUNMODE_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Execute operations are in the determination phase.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTATEND"></a><a id="msirunmode_rebootatend"></a><dl>
<dt><b>MSIRUNMODE_REBOOTATEND</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary after a successful installation (settable).

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTNOW"></a><a id="msirunmode_rebootnow"></a><dl>
<dt><b>MSIRUNMODE_REBOOTNOW</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary to continue the installation (settable).

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_CABINET"></a><a id="msirunmode_cabinet"></a><dl>
<dt><b>MSIRUNMODE_CABINET</b></dt>
</dl>
</td>
<td width="60%">
Files from cabinets and 
<a href="/windows/desktop/Msi/media-table">Media table</a> files are installing.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_SOURCESHORTNAMES"></a><a id="msirunmode_sourceshortnames"></a><dl>
<dt><b>MSIRUNMODE_SOURCESHORTNAMES</b></dt>
</dl>
</td>
<td width="60%">
The source LongFileNames is suppressed through the PID_MSISOURCE summary property.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_TARGETSHORTNAMES"></a><a id="msirunmode_targetshortnames"></a><dl>
<dt><b>MSIRUNMODE_TARGETSHORTNAMES</b></dt>
</dl>
</td>
<td width="60%">
The target LongFileNames is suppressed through the <a href="/windows/desktop/Msi/shortfilenames">SHORTFILENAMES</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_RESERVED11"></a><a id="msirunmode_reserved11"></a><dl>
<dt><b>MSIRUNMODE_RESERVED11</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_WINDOWS9X"></a><a id="msirunmode_windows9x"></a><dl>
<dt><b>MSIRUNMODE_WINDOWS9X</b></dt>
</dl>
</td>
<td width="60%">
The operating system is a 9x version.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_ZAWENABLED"></a><a id="msirunmode_zawenabled"></a><dl>
<dt><b>MSIRUNMODE_ZAWENABLED</b></dt>
</dl>
</td>
<td width="60%">
The operating system supports demand installation.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_RESERVED14"></a><a id="msirunmode_reserved14"></a><dl>
<dt><b>MSIRUNMODE_RESERVED14</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_RESERVED15"></a><a id="msirunmode_reserved15"></a><dl>
<dt><b>MSIRUNMODE_RESERVED15</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_SCHEDULED"></a><a id="msirunmode_scheduled"></a><dl>
<dt><b>MSIRUNMODE_SCHEDULED</b></dt>
</dl>
</td>
<td width="60%">
A custom action called from install script execution.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_ROLLBACK"></a><a id="msirunmode_rollback"></a><dl>
<dt><b>MSIRUNMODE_ROLLBACK</b></dt>
</dl>
</td>
<td width="60%">
A custom action called from rollback execution script.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_COMMIT"></a><a id="msirunmode_commit"></a><dl>
<dt><b>MSIRUNMODE_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
A custom action called from commit execution script.

</td>
</tr>
</table>

## -returns

<b>TRUE</b> indicates the specific property passed into the function is currently set.

<b>FALSE</b> indicates the specific property passed into the function is currently not set.

## -remarks

Note that not all the run mode values of <i>iRunMode</i> are available when calling 
<b>MsiGetMode</b> from a deferred custom action. For details, see 
<a href="/windows/desktop/Msi/obtaining-context-information-for-deferred-execution-custom-actions">Obtaining Context Information for Deferred Execution Custom Actions</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>