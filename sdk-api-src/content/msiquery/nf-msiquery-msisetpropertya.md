---
UID: NF:msiquery.MsiSetPropertyA
title: MsiSetPropertyA function (msiquery.h)
author: windows-sdk-content
description: The MsiSetProperty function sets the value for an installation property.
old-location: setup\msisetproperty.htm
tech.root: Msi
ms.assetid: f6376a19-579a-4e25-8ab6-bb66c623dd25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiSetProperty, MsiSetProperty function, MsiSetPropertyA, MsiSetPropertyW, _msi_msisetproperty, msiquery/MsiSetProperty, msiquery/MsiSetPropertyA, msiquery/MsiSetPropertyW, setup.msisetproperty
ms.topic: function
f1_keywords: 
 - "msiquery/MsiSetProperty"
dev_langs:
 - c++
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
 - MsiSetProperty
 - MsiSetPropertyA
 - MsiSetPropertyW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiSetPropertyA function


## -description


The 
<b>MsiSetProperty</b> function sets the value for an installation property.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer State Access Functions</a>
 

 

