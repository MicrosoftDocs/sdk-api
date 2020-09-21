---
UID: NF:msiquery.MsiVerifyDiskSpace
title: MsiVerifyDiskSpace function (msiquery.h)
description: The MsiVerifyDiskSpace function checks to see if sufficient disk space is present for the current installation.
helpviewer_keywords: ["MsiVerifyDiskSpace","MsiVerifyDiskSpace function","_msi_msiverifydiskspace","msiquery/MsiVerifyDiskSpace","setup.msiverifydiskspace"]
old-location: setup\msiverifydiskspace.htm
tech.root: setup
ms.assetid: 5b1ded22-37a4-4026-872a-20ac3a69fe86
ms.date: 12/05/2018
ms.keywords: MsiVerifyDiskSpace, MsiVerifyDiskSpace function, _msi_msiverifydiskspace, msiquery/MsiVerifyDiskSpace, setup.msiverifydiskspace
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
 - MsiVerifyDiskSpace
 - msiquery/MsiVerifyDiskSpace
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
 - MsiVerifyDiskSpace
---

# MsiVerifyDiskSpace function


## -description

The 
<b>MsiVerifyDiskSpace</b> function checks to see if sufficient disk space is present for the current installation.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

## -returns

This function returns UINT.

## -remarks

See 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Selection Functions</a>