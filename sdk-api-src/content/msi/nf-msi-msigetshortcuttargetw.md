---
UID: NF:msi.MsiGetShortcutTargetW
title: MsiGetShortcutTargetW function
author: windows-sdk-content
description: The MsiGetShortcutTarget function examines a shortcut and returns its product, feature name, and component if available.
old-location: setup\msigetshortcuttarget.htm
tech.root: msi
ms.assetid: 5c040372-d266-4f79-9b80-950ceac9f9b8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MsiGetShortcutTarget, MsiGetShortcutTarget function, MsiGetShortcutTargetA, MsiGetShortcutTargetW, _msi_msigetshortcuttarget, msi/MsiGetShortcutTarget, msi/MsiGetShortcutTargetA, msi/MsiGetShortcutTargetW, setup.msigetshortcuttarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


### -param szFeatureId [out]

The feature name of the shortcut. The string buffer must be MAX_FEATURE_CHARS+1 characters long. This parameter can be null.


### -param szComponentCode [out]

A GUID of the component code. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


## -returns



This function returns UINT.




## -remarks



If the function fails, and the shortcut exists, the regular contents of the shortcut may be accessed through the 
<a href="_win32_ishelllink_cpp">IShellLink</a> interface.

Otherwise, the state of the target may be determined by using the 
<a href="database_functions.htm">Installer Selection Functions</a>.



