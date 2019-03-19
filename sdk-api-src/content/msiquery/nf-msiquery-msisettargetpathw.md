---
UID: NF:msiquery.MsiSetTargetPathW
title: MsiSetTargetPathW function (msiquery.h)
author: windows-sdk-content
description: The MsiSetTargetPath function sets the full target path for a folder in the Directory table.
old-location: setup\msisettargetpath.htm
tech.root: Msi
ms.assetid: bfd39656-4901-442f-940d-424d440caf70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MsiSetTargetPath, MsiSetTargetPath function, MsiSetTargetPathA, MsiSetTargetPathW, _msi_msisettargetpath, msiquery/MsiSetTargetPath, msiquery/MsiSetTargetPathA, msiquery/MsiSetTargetPathW, setup.msisettargetpath
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiSetTargetPathW function


## -description


The 
<b>MsiSetTargetPath</b> function sets the full target path for a folder in the 
<a href="https://msdn.microsoft.com/eaca30cb-fec1-49ca-8b23-5e54c583e3e2">Directory table</a>.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


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
<a href="https://msdn.microsoft.com/eaca30cb-fec1-49ca-8b23-5e54c583e3e2">Directory table</a>. Also, the path specifications of all other path objects in the table that are either subordinate or equivalent to the changed path are updated to reflect the change. The properties for each affected path are also updated.

<b>MsiSetTargetPath</b> fails if the selected directory is read only.

If an error occurs in this function, all updated paths and properties revert to their previous values. Therefore, it is safe to treat errors returned by this function as nonfatal.

Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user. Check the 
<a href="https://msdn.microsoft.com/833e9a15-10f8-4b1c-945f-bc02b506f627">ProductState</a> property before calling 
<b>MsiSetTargetPath</b> to determine if the product containing this component is installed.

See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer Location Functions</a>
 

 

