---
UID: NF:msi.MsiUseFeatureA
title: MsiUseFeatureA function (msi.h)
description: The MsiUseFeature function increments the usage count for a particular feature and indicates the installation state for that feature. This function should be used to indicate an application's intent to use a feature. (ANSI)
helpviewer_keywords: ["MsiUseFeatureA", "msi/MsiUseFeatureA"]
old-location: setup\msiusefeature.htm
tech.root: setup
ms.assetid: 7a4dc671-d82e-4775-8198-79b80a4dd9e4
ms.date: 12/05/2018
ms.keywords: MsiUseFeature, MsiUseFeature function, MsiUseFeatureA, MsiUseFeatureW, _msi_msiusefeature, msi/MsiUseFeature, msi/MsiUseFeatureA, msi/MsiUseFeatureW, setup.msiusefeature
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiUseFeatureW (Unicode) and MsiUseFeatureA (ANSI)
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
 - MsiUseFeatureA
 - msi/MsiUseFeatureA
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
 - MsiUseFeature
 - MsiUseFeatureA
 - MsiUseFeatureW
---

# MsiUseFeatureA function


## -description

The 
<b>MsiUseFeature</b> function increments the usage count for a particular feature and indicates the installation state for that feature. This function should be used to indicate an application's intent to use a feature.

## -parameters

### -param szProduct [in]

Specifies the product code for the product that owns the feature to be used.

### -param szFeature [in]

Identifies the feature to be used.

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
<dt><b>INSTALLSTATE_BADCONFIG</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid function argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is locally installed and available for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed from the source and available for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The feature is not published.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
<b>MsiUseFeature</b> function should only be used on features known to be published. INSTALLSTATE_UNKNOWN indicates that the program is trying to use a feature that is not published. The application should determine whether the feature is published before calling 
<b>MsiUseFeature</b> by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea">MsiQueryFeatureState</a> or 
<a href="/windows/desktop/api/msi/nf-msi-msienumfeaturesa">MsiEnumFeatures</a>. The application should make these calls while it initializes. An application should only use features that are known to be published.





> [!NOTE]
> The msi.h header defines MsiUseFeature as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Application-Only Functions</a>
