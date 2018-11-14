---
UID: NF:msiquery.MsiGetLanguage
title: MsiGetLanguage function
author: windows-sdk-content
description: The MsiGetLanguage function returns the numeric language of the installation that is currently running.
old-location: setup\msigetlanguage.htm
tech.root: msi
ms.assetid: e959dbdc-141c-41be-8752-220aa8e96064
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MsiGetLanguage, MsiGetLanguage function, _msi_msigetlanguage, msiquery/MsiGetLanguage, setup.msigetlanguage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiGetLanguage
: 
---

# MsiGetLanguage function


## -description


The 
<b>MsiGetLanguage</b> function returns the numeric language of the installation that is currently running.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


## -returns



If the function succeeds, the return value is the numeric LANGID for the install.

If the function fails, the return value can be the following value.




## -remarks



The 
<b>MsiGetLanguage</b> function returns 0 if an installation is not running.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer State Access Functions</a>
 

 

