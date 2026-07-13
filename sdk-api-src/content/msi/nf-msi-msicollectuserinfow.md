---
UID: NF:msi.MsiCollectUserInfoW
title: MsiCollectUserInfoW function (msi.h)
description: The MsiCollectUserInfo function obtains and stores the user information and product ID from an installation wizard. (Unicode)
helpviewer_keywords: ["MsiCollectUserInfo", "MsiCollectUserInfo function", "MsiCollectUserInfoW", "_msi_msicollectuserinfo", "msi/MsiCollectUserInfo", "msi/MsiCollectUserInfoW", "setup.msicollectuserinfo"]
old-location: setup\msicollectuserinfo.htm
tech.root: setup
ms.assetid: a8be3c24-cd5a-4da9-abe7-b0e40a87a07f
ms.date: 12/05/2018
ms.keywords: MsiCollectUserInfo, MsiCollectUserInfo function, MsiCollectUserInfoA, MsiCollectUserInfoW, _msi_msicollectuserinfo, msi/MsiCollectUserInfo, msi/MsiCollectUserInfoA, msi/MsiCollectUserInfoW, setup.msicollectuserinfo
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiCollectUserInfoW (Unicode) and MsiCollectUserInfoA (ANSI)
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
 - MsiCollectUserInfoW
 - msi/MsiCollectUserInfoW
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
 - MsiCollectUserInfo
 - MsiCollectUserInfoA
 - MsiCollectUserInfoW
---

# MsiCollectUserInfoW function


## -description

The 
<b>MsiCollectUserInfo</b> function obtains and stores the user information and product ID from an installation wizard.

## -parameters

### -param szProduct [in]

Specifies the product code of the product for which the user information is collected.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="/windows/desktop/Msi/error-codes">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An error relating to initialization occurred.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
<b>MsiCollectUserInfo</b> function is typically called by an application during the first run of the application. The application first calls 
<a href="/windows/desktop/api/msi/nf-msi-msigetuserinfoa">MsiGetUserInfo</a>. If that call fails, the application calls 
<b>MsiCollectUserInfo</b>. 
<b>MsiCollectUserInfo</b> opens the product's installation package and invokes a wizard sequence that collects user information. Upon completion of the sequence, user information is registered. Since this API requires an authored user interface, the user interface level should be set to full by calling 
<a href="/windows/desktop/api/msi/nf-msi-msisetinternalui">MsiSetInternalUI</a> as INSTALLUILEVEL_FULL.

The 
<b>MsiCollectUserInfo</b> invokes a 
<a href="/windows/desktop/Msi/firstrun-dialog">FirstRun Dialog</a>.





> [!NOTE]
> The msi.h header defines MsiCollectUserInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Application-Only Functions</a>



<a href="/windows/desktop/Msi/error-codes">Error Codes</a>



<a href="/windows/desktop/Msi/initialization-errors">Initialization Error</a>
