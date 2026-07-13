---
UID: NF:msiquery.MsiSetTargetPathW
title: MsiSetTargetPathW function (msiquery.h)
description: The MsiSetTargetPath function sets the full target path for a folder in the Directory table. (Unicode)
helpviewer_keywords: ["MsiSetTargetPath", "MsiSetTargetPath function", "MsiSetTargetPathW", "_msi_msisettargetpath", "msiquery/MsiSetTargetPath", "msiquery/MsiSetTargetPathW", "setup.msisettargetpath"]
old-location: setup\msisettargetpath.htm
tech.root: setup
ms.assetid: bfd39656-4901-442f-940d-424d440caf70
ms.date: 12/05/2018
ms.keywords: MsiSetTargetPath, MsiSetTargetPath function, MsiSetTargetPathA, MsiSetTargetPathW, _msi_msisettargetpath, msiquery/MsiSetTargetPath, msiquery/MsiSetTargetPathA, msiquery/MsiSetTargetPathW, setup.msisettargetpath
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetTargetPathW (Unicode) and MsiSetTargetPathA (ANSI)
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
 - MsiSetTargetPathW
 - msiquery/MsiSetTargetPathW
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
 - MsiSetTargetPath
 - MsiSetTargetPathA
 - MsiSetTargetPathW
---

# MsiSetTargetPathW function


## -description

The 
<b>MsiSetTargetPath</b> function sets the full target path for a folder in the 
<a href="/windows/desktop/Msi/directory-table">Directory table</a>.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szFolder [in]

Specifies the folder identifier. This is a primary key in the Directory table.

### -param szFolderPath [in]

Specifies the full path for the folder, ending in a directory separator.

## -returns

The 
<b>MsiSetTargetPath</b> function returns the following values:

## -remarks

The 
<b>MsiSetTargetPath</b> function changes the path specification for the target directory named in the in-memory 
<a href="/windows/desktop/Msi/directory-table">Directory table</a>. Also, the path specifications of all other path objects in the table that are either subordinate or equivalent to the changed path are updated to reflect the change. The properties for each affected path are also updated.

<b>MsiSetTargetPath</b> fails if the selected directory is read only.

If an error occurs in this function, all updated paths and properties revert to their previous values. Therefore, it is safe to treat errors returned by this function as nonfatal.

Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user. Check the 
<a href="/windows/desktop/Msi/productstate">ProductState</a> property before calling 
<b>MsiSetTargetPath</b> to determine if the product containing this component is installed.

See 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiSetTargetPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Location Functions</a>
