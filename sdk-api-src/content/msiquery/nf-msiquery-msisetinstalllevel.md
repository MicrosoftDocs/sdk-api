---
UID: NF:msiquery.MsiSetInstallLevel
title: MsiSetInstallLevel function (msiquery.h)
description: The MsiSetInstallLevel function sets the installation level for a full product installation.
helpviewer_keywords: ["MsiSetInstallLevel","MsiSetInstallLevel function","_msi_msisetinstalllevel","msiquery/MsiSetInstallLevel","setup.msisetinstalllevel"]
old-location: setup\msisetinstalllevel.htm
tech.root: setup
ms.assetid: 98f1d91d-632e-4dea-948f-2dc416b4d410
ms.date: 12/05/2018
ms.keywords: MsiSetInstallLevel, MsiSetInstallLevel function, _msi_msisetinstalllevel, msiquery/MsiSetInstallLevel, setup.msisetinstalllevel
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
 - MsiSetInstallLevel
 - msiquery/MsiSetInstallLevel
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
 - MsiSetInstallLevel
---

# MsiSetInstallLevel function


## -description

The 
<b>MsiSetInstallLevel</b> function sets the installation level for a full product installation.

## -parameters

### -param hInstall [in]

Handle to the installation that is provided to a DLL custom action or obtained by using <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param iInstallLevel [in]

The installation level.

## -returns

The 
<b>MsiSetInstallLevel</b> function returns one of the following values:

## -remarks

The 
<b>MsiSetInstallLevel</b> function sets the following:

<ul>
<li>The installation level for the current installation to a specified value.</li>
<li>The Select and Installed states for all features in the 
<a href="/windows/desktop/Msi/feature-table">Feature table</a>.</li>
<li>The Action state of each component in the 
<a href="/windows/desktop/Msi/component-table">Component table</a>, based on the new level.</li>
</ul>
For any installation, there is a defined install level, which is an integral value from 1 to 32,767. The initial value is determined by the 
<a href="/windows/desktop/Msi/installlevel">INSTALLLEVEL</a> property, which is set in the 
<a href="/windows/desktop/Msi/property-table">Property Table</a>.

If 0 (zero) or a negative number is passed in the <i>iInstallLevel</i> parameter, the current installation level does not change, but all features are still updated based on the current installation level. For more information, see 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Selection Functions</a>