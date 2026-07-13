---
UID: NF:msi.MsiQueryFeatureStateA
title: MsiQueryFeatureStateA function (msi.h)
description: The MsiQueryFeatureState function returns the installed state for a product feature. (ANSI)
helpviewer_keywords: ["MsiQueryFeatureStateA", "msi/MsiQueryFeatureStateA"]
old-location: setup\msiqueryfeaturestate.htm
tech.root: setup
ms.assetid: d84aa7f1-d29a-493d-a065-8f7b680019d7
ms.date: 12/05/2018
ms.keywords: MsiQueryFeatureState, MsiQueryFeatureState function, MsiQueryFeatureStateA, MsiQueryFeatureStateW, _msi_msiqueryfeaturestate, msi/MsiQueryFeatureState, msi/MsiQueryFeatureStateA, msi/MsiQueryFeatureStateW, setup.msiqueryfeaturestate
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiQueryFeatureStateW (Unicode) and MsiQueryFeatureStateA (ANSI)
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
 - MsiQueryFeatureStateA
 - msi/MsiQueryFeatureStateA
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
 - MsiQueryFeatureState
 - MsiQueryFeatureStateA
 - MsiQueryFeatureStateW
---

# MsiQueryFeatureStateA function


## -description

The 
<b>MsiQueryFeatureState</b> function returns the installed state for a product feature.

## -parameters

### -param szProduct [in]

Specifies the product code for the product that contains the feature of interest.

### -param szFeature [in]

Identifies the feature of interest.

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
The feature is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The feature is advertised

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed to run from source.

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
The product code or feature ID is unknown.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
<b>MsiQueryFeatureState</b> function does not validate that the feature is actually accessible.





> [!NOTE]
> The msi.h header defines MsiQueryFeatureState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
