---
UID: NF:msiquery.MsiSetPropertyA
title: MsiSetPropertyA function
author: windows-sdk-content
description: The MsiSetProperty function sets the value for an installation property.
old-location: setup\msisetproperty.htm
old-project: Msi
ms.assetid: f6376a19-579a-4e25-8ab6-bb66c623dd25
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiSetProperty, MsiSetProperty function, MsiSetPropertyA, MsiSetPropertyW, _msi_msisetproperty, msiquery/MsiSetProperty, msiquery/MsiSetPropertyA, msiquery/MsiSetPropertyW, setup.msisetproperty
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
req.unicode-ansi: MsiSetPropertyW (Unicode) and MsiSetPropertyA (ANSI)
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
 - MsiSetProperty
 - MsiSetPropertyA
 - MsiSetPropertyW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSetPropertyA function


## -description


The 
<b>MsiSetProperty</b> function sets the value for an installation property.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szName [in]

Specifies the name of the property.


### -param szValue [in]

Specifies the value of the property.


## -returns



This function returns UINT.




## -remarks



If the property is not defined, it is created by the 
<b>MsiSetProperty</b> function. If the value is null or an empty string, the property is removed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop//Msi/database-functions">Installer State Access Functions</a>
 

 

