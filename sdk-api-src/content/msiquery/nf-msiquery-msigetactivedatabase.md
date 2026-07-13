---
UID: NF:msiquery.MsiGetActiveDatabase
title: MsiGetActiveDatabase function (msiquery.h)
description: The MsiGetActiveDatabase function returns the active database for the installation. This function returns a read-only handle that should be closed using MsiCloseHandle.
helpviewer_keywords: ["MsiGetActiveDatabase","MsiGetActiveDatabase function","_msi_msigetactivedatabase","msiquery/MsiGetActiveDatabase","setup.msigetactivedatabase"]
old-location: setup\msigetactivedatabase.htm
tech.root: setup
ms.assetid: 148d467f-fecd-42a9-b838-22799a159f97
ms.date: 12/05/2018
ms.keywords: MsiGetActiveDatabase, MsiGetActiveDatabase function, _msi_msigetactivedatabase, msiquery/MsiGetActiveDatabase, setup.msigetactivedatabase
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
 - MsiGetActiveDatabase
 - msiquery/MsiGetActiveDatabase
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
 - MsiGetActiveDatabase
---

# MsiGetActiveDatabase function


## -description

The 
<b>MsiGetActiveDatabase</b> function returns the active database for the installation. This function returns a read-only handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

## -returns

If the function succeeds, it returns a read-only handle to the database currently in use by the installer. If the function fails, the function returns zero, 0.

## -remarks

The 
<b>MsiGetActiveDatabase</b> function accesses the database in use by the running the installation.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>