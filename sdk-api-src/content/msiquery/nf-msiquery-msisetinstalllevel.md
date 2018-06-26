---
UID: NF:msiquery.MsiSetInstallLevel
title: MsiSetInstallLevel function
author: windows-sdk-content
description: The MsiSetInstallLevel function sets the installation level for a full product installation.
old-location: setup\msisetinstalllevel.htm
old-project: Msi
ms.assetid: 98f1d91d-632e-4dea-948f-2dc416b4d410
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: MsiSetInstallLevel, MsiSetInstallLevel function, _msi_msisetinstalllevel, msiquery/MsiSetInstallLevel, setup.msisetinstalllevel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiSetInstallLevel
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSetInstallLevel function


## -description


The 
<b>MsiSetInstallLevel</b> function sets the installation level for a full product installation.


## -parameters




### -param hInstall [in]

Handle to the installation that is provided to a DLL custom action or obtained by using <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param iInstallLevel [in]

The installation level.


## -returns



The 
<b>MsiSetInstallLevel</b> function returns one of the following values:
					




## -remarks



The 
<b>MsiSetInstallLevel</b> function sets the following:

<ul>
<li>The installation level for the current installation to a specified value.</li>
<li>The Select and Installed states for all features in the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a>.</li>
<li>The Action state of each component in the 
<a href="https://msdn.microsoft.com/069d64e9-106a-42b7-8dea-a44fc0c6e0cd">Component table</a>, based on the new level.</li>
</ul>
For any installation, there is a defined install level, which is an integral value from 1 to 32,767. The initial value is determined by the 
<a href="https://msdn.microsoft.com/5051cc46-837a-4446-a54c-4bd4081a424c">INSTALLLEVEL</a> property, which is set in the 
<a href="https://msdn.microsoft.com/1f4215b2-dc71-4e6e-bc2e-3b43316806b9">Property Table</a>.

If 0 (zero) or a negative number is passed in the <i>iInstallLevel</i> parameter, the current installation level does not change, but all features are still updated based on the current installation level. For more information, see 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Installer Selection Functions</a>
 

 

