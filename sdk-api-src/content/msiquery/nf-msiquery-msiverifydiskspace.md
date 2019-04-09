---
UID: NF:msiquery.MsiVerifyDiskSpace
title: MsiVerifyDiskSpace function (msiquery.h)
author: windows-sdk-content
description: The MsiVerifyDiskSpace function checks to see if sufficient disk space is present for the current installation.
old-location: setup\msiverifydiskspace.htm
tech.root: Msi
ms.assetid: 5b1ded22-37a4-4026-872a-20ac3a69fe86
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiVerifyDiskSpace, MsiVerifyDiskSpace function, _msi_msiverifydiskspace, msiquery/MsiVerifyDiskSpace, setup.msiverifydiskspace
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiVerifyDiskSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiVerifyDiskSpace function


## -description


The 
<b>MsiVerifyDiskSpace</b> function checks to see if sufficient disk space is present for the current installation.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


## -returns



This function returns UINT.




## -remarks



See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer Selection Functions</a>
 

 

