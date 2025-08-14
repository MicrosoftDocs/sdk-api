---
UID: NF:msi.MsiQueryProductStateW
title: MsiQueryProductStateW function (msi.h)
description: The MsiQueryProductState function returns the installed state for a product. (Unicode)
helpviewer_keywords: ["MsiQueryProductState", "MsiQueryProductState function", "MsiQueryProductStateW", "_msi_msiqueryproductstate", "msi/MsiQueryProductState", "msi/MsiQueryProductStateW", "setup.msiqueryproductstate"]
old-location: setup\msiqueryproductstate.htm
tech.root: setup
ms.assetid: f26f3229-d1ce-4802-99b1-857c6501c828
ms.date: 12/05/2018
ms.keywords: MsiQueryProductState, MsiQueryProductState function, MsiQueryProductStateA, MsiQueryProductStateW, _msi_msiqueryproductstate, msi/MsiQueryProductState, msi/MsiQueryProductStateA, msi/MsiQueryProductStateW, setup.msiqueryproductstate
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiQueryProductStateW (Unicode) and MsiQueryProductStateA (ANSI)
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
 - MsiQueryProductStateW
 - msi/MsiQueryProductStateW
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
 - MsiQueryProductState
 - MsiQueryProductStateA
 - MsiQueryProductStateW
---

# MsiQueryProductStateW function


## -description

The 
<b>MsiQueryProductState</b> function returns the installed state for a product.

## -parameters

### -param szProduct [in]

Specifies the product code that identifies the product to be queried.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The product is installed for a different user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The product is advertised but not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The product is installed for the current user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product is neither advertised or installed.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiQueryProductState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
