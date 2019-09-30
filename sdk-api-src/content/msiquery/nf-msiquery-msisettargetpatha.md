---
UID: NF:msiquery.MsiSetTargetPathA
title: MsiSetTargetPathA function (msiquery.h)
author: windows-sdk-content
description: The MsiSetTargetPath function sets the full target path for a folder in the Directory table.
old-location: setup\msisettargetpath.htm
tech.root: Msi
ms.assetid: bfd39656-4901-442f-940d-424d440caf70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiSetTargetPath, MsiSetTargetPath function, MsiSetTargetPathA, MsiSetTargetPathW, _msi_msisettargetpath, msiquery/MsiSetTargetPath, msiquery/MsiSetTargetPathA, msiquery/MsiSetTargetPathW, setup.msisettargetpath
ms.topic: function
f1_keywords: 
 - "msiquery/MsiSetTargetPath"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiSetTargetPathA function


## -description


The 
<b>MsiSetTargetPath</b> function sets the full target path for a folder in the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/directory-table">Directory table</a>.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/Msi/directory-table">Directory table</a>. Also, the path specifications of all other path objects in the table that are either subordinate or equivalent to the changed path are updated to reflect the change. The properties for each affected path are also updated.

<b>MsiSetTargetPath</b> fails if the selected directory is read only.

If an error occurs in this function, all updated paths and properties revert to their previous values. Therefore, it is safe to treat errors returned by this function as nonfatal.

Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user. Check the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/productstate">ProductState</a> property before calling 
<b>MsiSetTargetPath</b> to determine if the product containing this component is installed.

See 
<a href="https://docs.microsoft.com/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer Location Functions</a>
 

 

