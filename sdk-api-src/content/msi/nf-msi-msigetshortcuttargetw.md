---
UID: NF:msi.MsiGetShortcutTargetW
title: MsiGetShortcutTargetW function
author: windows-sdk-content
description: The MsiGetShortcutTarget function examines a shortcut and returns its product, feature name, and component if available.
old-location: setup\msigetshortcuttarget.htm
old-project: Msi
ms.assetid: 5c040372-d266-4f79-9b80-950ceac9f9b8
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: MsiGetShortcutTarget, MsiGetShortcutTarget function, MsiGetShortcutTargetA, MsiGetShortcutTargetW, _msi_msigetshortcuttarget, msi/MsiGetShortcutTarget, msi/MsiGetShortcutTargetA, msi/MsiGetShortcutTargetW, setup.msigetshortcuttarget
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetShortcutTargetW function


## -description


The 
<b>MsiGetShortcutTarget</b> function examines a shortcut and returns its product, feature name, and component if available.


## -parameters




### -param szShortcutPath

TBD


### -param szProductCode [out]

A GUID for the product code of the shortcut. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


### -param szFeatureId [out]

The feature name of the shortcut. The string buffer must be MAX_FEATURE_CHARS+1 characters long. This parameter can be null.


### -param szComponentCode [out]

A GUID of the component code. This string buffer must be 39 characters long. The first 38 characters are for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>, and the last character is for the terminating null character. This parameter can be null.


#### - szShortcutTarget [in]

A null-terminated string specifying the full path to a shortcut.


## -returns



This function returns UINT.




## -remarks



If the function fails, and the shortcut exists, the regular contents of the shortcut may be accessed through the 
<a href="https://msdn.microsoft.com/library/Bb774950(v=VS.85).aspx">IShellLink</a> interface.

Otherwise, the state of the target may be determined by using the 
<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Installer Selection Functions</a>.



