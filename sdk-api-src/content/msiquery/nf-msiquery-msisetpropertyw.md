---
UID: NF:msiquery.MsiSetPropertyW
title: MsiSetPropertyW function (msiquery.h)
description: The MsiSetProperty function sets the value for an installation property. (Unicode)
helpviewer_keywords: ["MsiSetProperty", "MsiSetProperty function", "MsiSetPropertyW", "_msi_msisetproperty", "msiquery/MsiSetProperty", "msiquery/MsiSetPropertyW", "setup.msisetproperty"]
old-location: setup\msisetproperty.htm
tech.root: setup
ms.assetid: f6376a19-579a-4e25-8ab6-bb66c623dd25
ms.date: 12/05/2018
ms.keywords: MsiSetProperty, MsiSetProperty function, MsiSetPropertyA, MsiSetPropertyW, _msi_msisetproperty, msiquery/MsiSetProperty, msiquery/MsiSetPropertyA, msiquery/MsiSetPropertyW, setup.msisetproperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSetPropertyW
 - msiquery/MsiSetPropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiSetProperty
 - MsiSetPropertyA
 - MsiSetPropertyW
---

# MsiSetPropertyW function


## -description

The 
<b>MsiSetProperty</b> function sets the value for an installation property.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szName [in]

Specifies the name of the property.

### -param szValue [in]

Specifies the value of the property.

## -returns

This function returns UINT.

## -remarks

If the property is not defined, it is created by the 
<b>MsiSetProperty</b> function. If the value is null or an empty string, the property is removed.





> [!NOTE]
> The msiquery.h header defines MsiSetProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>
