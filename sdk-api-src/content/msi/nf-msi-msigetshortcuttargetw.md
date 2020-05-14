---
UID: NF:msi.MsiGetShortcutTargetW
title: MsiGetShortcutTargetW function (msi.h)
description: The MsiGetShortcutTarget function examines a shortcut and returns its product, feature name, and component if available.helpviewer_keywords: ["MsiGetShortcutTarget","MsiGetShortcutTarget function","MsiGetShortcutTargetA","MsiGetShortcutTargetW","_msi_msigetshortcuttarget","msi/MsiGetShortcutTarget","msi/MsiGetShortcutTargetA","msi/MsiGetShortcutTargetW","setup.msigetshortcuttarget"]
old-location: setup\msigetshortcuttarget.htm
tech.root: Msi
ms.assetid: 5c040372-d266-4f79-9b80-950ceac9f9b8
ms.date: 12/05/2018
ms.keywords: MsiGetShortcutTarget, MsiGetShortcutTarget function, MsiGetShortcutTargetA, MsiGetShortcutTargetW, _msi_msigetshortcuttarget, msi/MsiGetShortcutTarget, msi/MsiGetShortcutTargetA, msi/MsiGetShortcutTargetW, setup.msigetshortcuttarget
f1_keywords:
- msi/MsiGetShortcutTarget
dev_langs:
- c++
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetShortcutTargetW (Unicode) and MsiGetShortcutTargetA (ANSI)
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
- MsiGetShortcutTarget
- MsiGetShortcutTargetA
- MsiGetShortcutTargetW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiGetShortcutTargetW function


## -description


The 
<b>MsiGetShortcutTarget</b> function examines a shortcut and returns its product, feature name, and component if available.


## -parameters




### -param szShortcutPath [in]

A null-terminated string specifying the full path to a shortcut.


### -param szProductCode [out]

A GUID for the product code of the shortcut. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/guid">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


### -param szFeatureId [out]

The feature name of the shortcut. The string buffer must be MAX_FEATURE_CHARS+1 characters long. This parameter can be null.


### -param szComponentCode [out]

A GUID of the component code. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/guid">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


## -returns



This function returns UINT.




## -remarks



If the function fails, and the shortcut exists, the regular contents of the shortcut may be accessed through the 
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> interface.

Otherwise, the state of the target may be determined by using the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer Selection Functions</a>.



