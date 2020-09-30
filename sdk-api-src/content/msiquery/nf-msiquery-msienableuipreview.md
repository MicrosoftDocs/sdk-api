---
UID: NF:msiquery.MsiEnableUIPreview
title: MsiEnableUIPreview function (msiquery.h)
description: The MsiEnableUIPreview function enables preview mode of the user interface to facilitate authoring of user-interface dialog boxes. This function returns a handle that should be closed using MsiCloseHandle.
helpviewer_keywords: ["MsiEnableUIPreview","MsiEnableUIPreview function","_msi_msienableuipreview","msiquery/MsiEnableUIPreview","setup.msienableuipreview"]
old-location: setup\msienableuipreview.htm
tech.root: setup
ms.assetid: 77df6829-119d-4fe6-96b0-c75381b9de6c
ms.date: 12/05/2018
ms.keywords: MsiEnableUIPreview, MsiEnableUIPreview function, _msi_msienableuipreview, msiquery/MsiEnableUIPreview, setup.msienableuipreview
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
 - MsiEnableUIPreview
 - msiquery/MsiEnableUIPreview
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
 - MsiEnableUIPreview
---

# MsiEnableUIPreview function


## -description

The 
<b>MsiEnableUIPreview</b> function enables preview mode of the user interface to facilitate authoring of user-interface dialog boxes. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hDatabase [in]

Handle to the database.

### -param phPreview [out]

Pointer to a returned handle for user-interface preview capability.

## -returns

This function returns UINT.

## -remarks

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">User Interface Functions</a>