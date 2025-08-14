---
UID: NF:msiquery.MsiSetMode
title: MsiSetMode function (msiquery.h)
description: The MsiSetMode function sets an internal engine Boolean state.
helpviewer_keywords: ["MSIRUNMODE_REBOOTATEND","MSIRUNMODE_REBOOTNOW","MsiSetMode","MsiSetMode function","_msi_msisetmode","msiquery/MsiSetMode","setup.msisetmode"]
old-location: setup\msisetmode.htm
tech.root: setup
ms.assetid: bf0eef83-8ef4-4107-b598-ccc50b179858
ms.date: 12/05/2018
ms.keywords: MSIRUNMODE_REBOOTATEND, MSIRUNMODE_REBOOTNOW, MsiSetMode, MsiSetMode function, _msi_msisetmode, msiquery/MsiSetMode, setup.msisetmode
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
 - MsiSetMode
 - msiquery/MsiSetMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiSetMode
---

# MsiSetMode function


## -description

The 
<b>MsiSetMode</b> function sets an internal engine Boolean state.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param eRunMode [in]

Specifies the run mode. This parameter must be one of the following values. While there are many values for this parameter, as described in 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetmode">MsiGetMode</a>, only one of the following values can be set. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTATEND"></a><a id="msirunmode_rebootatend"></a><dl>
<dt><b>MSIRUNMODE_REBOOTATEND</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary after a successful installation.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTNOW"></a><a id="msirunmode_rebootnow"></a><dl>
<dt><b>MSIRUNMODE_REBOOTNOW</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary to continue installation.

</td>
</tr>
</table>

### -param fState [in]

Specifies the state to set to <b>TRUE</b> or <b>FALSE</b>.

## -returns

This function returns UINT.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>