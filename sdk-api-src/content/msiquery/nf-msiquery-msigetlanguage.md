---
UID: NF:msiquery.MsiGetLanguage
title: MsiGetLanguage function (msiquery.h)
description: The MsiGetLanguage function returns the numeric language of the installation that is currently running.
helpviewer_keywords: ["MsiGetLanguage","MsiGetLanguage function","_msi_msigetlanguage","msiquery/MsiGetLanguage","setup.msigetlanguage"]
old-location: setup\msigetlanguage.htm
tech.root: setup
ms.assetid: e959dbdc-141c-41be-8752-220aa8e96064
ms.date: 12/05/2018
ms.keywords: MsiGetLanguage, MsiGetLanguage function, _msi_msigetlanguage, msiquery/MsiGetLanguage, setup.msigetlanguage
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
 - MsiGetLanguage
 - msiquery/MsiGetLanguage
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
 - MsiGetLanguage
---

# MsiGetLanguage function


## -description

The 
<b>MsiGetLanguage</b> function returns the numeric language of the installation that is currently running.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

## -returns

If the function succeeds, the return value is the numeric LANGID for the install.

If the function fails, the return value can be the following value.

## -remarks

The 
<b>MsiGetLanguage</b> function returns 0 if an installation is not running.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>