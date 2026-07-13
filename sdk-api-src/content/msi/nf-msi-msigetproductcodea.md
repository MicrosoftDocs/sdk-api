---
UID: NF:msi.MsiGetProductCodeA
title: MsiGetProductCodeA function (msi.h)
description: The MsiGetProductCode function returns the product code of an application by using the component code of an installed or advertised component of the application. (ANSI)
helpviewer_keywords: ["MsiGetProductCodeA", "msi/MsiGetProductCodeA"]
old-location: setup\msigetproductcode.htm
tech.root: setup
ms.assetid: 5893c437-6827-44d6-bc22-18c402dda894
ms.date: 12/05/2018
ms.keywords: MsiGetProductCode, MsiGetProductCode function, MsiGetProductCodeA, MsiGetProductCodeW, _msi_msigetproductcode, msi/MsiGetProductCode, msi/MsiGetProductCodeA, msi/MsiGetProductCodeW, setup.msigetproductcode
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetProductCodeW (Unicode) and MsiGetProductCodeA (ANSI)
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
 - MsiGetProductCodeA
 - msi/MsiGetProductCodeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetProductCode
 - MsiGetProductCodeA
 - MsiGetProductCodeW
---

# MsiGetProductCodeA function


## -description

The 
<b>MsiGetProductCode</b> function returns the product code of an application by using the component code of an installed or advertised component of the application. During initialization, an application must determine under which product code it has been installed or advertised.

## -parameters

### -param szComponent [in]

This parameter specifies the component code of a component that has been installed by the application. This will be typically the component code of the component containing the executable file of the application.

### -param lpBuf39 [out]

Pointer to a buffer that receives the product code. This buffer must be 39 characters long. The first 38 characters are for the GUID, and the last character is for the terminating null character.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The product code could not be determined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The specified component is unknown.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

During initialization, an application must determine the product code under which it was installed. An application can be part of different products in different installations. For example, an application can be part of a suite of applications, or it can be installed by itself.





> [!NOTE]
> The msi.h header defines MsiGetProductCode as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Application-Only Functions</a>
