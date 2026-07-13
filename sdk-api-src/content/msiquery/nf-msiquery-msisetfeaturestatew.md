---
UID: NF:msiquery.MsiSetFeatureStateW
title: MsiSetFeatureStateW function (msiquery.h)
description: The MsiSetFeatureState function sets a feature to a specified state. (Unicode)
helpviewer_keywords: ["INSTALLSTATE_ABSENT", "INSTALLSTATE_ADVERTISED", "INSTALLSTATE_LOCAL", "INSTALLSTATE_SOURCE", "MsiSetFeatureState", "MsiSetFeatureState function", "MsiSetFeatureStateW", "_msi_msisetfeaturestate", "msiquery/MsiSetFeatureState", "msiquery/MsiSetFeatureStateW", "setup.msisetfeaturestate"]
old-location: setup\msisetfeaturestate.htm
tech.root: setup
ms.assetid: c7b22484-5a89-44f2-b0ff-6061a7fc5703
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiSetFeatureState, MsiSetFeatureState function, MsiSetFeatureStateA, MsiSetFeatureStateW, _msi_msisetfeaturestate, msiquery/MsiSetFeatureState, msiquery/MsiSetFeatureStateA, msiquery/MsiSetFeatureStateW, setup.msisetfeaturestate
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetFeatureStateW (Unicode) and MsiSetFeatureStateA (ANSI)
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
 - MsiSetFeatureStateW
 - msiquery/MsiSetFeatureStateW
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
 - MsiSetFeatureState
 - MsiSetFeatureStateA
 - MsiSetFeatureStateW
---

# MsiSetFeatureStateW function


## -description

The 
<b>MsiSetFeatureState</b> function sets a feature to a specified state.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szFeature [in]

Specifies the name of the feature.

### -param iState [in]

Specifies the state to set. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The feature is not installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is run from the source, CD, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The feature is advertised.

</td>
</tr>
</table>

## -returns

The 
<b>MsiSetFeatureState</b> function returns the following values:

## -remarks

The 
<b>MsiSetFeatureState</b> function requests a change in the select state of a feature in the 
<a href="/windows/desktop/Msi/feature-table">Feature</a> table and its children. In turn, the action state of all the components linked to the changed feature records are also updated appropriately, based on the new feature select state.

The 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisetinstalllevel">MsiSetInstallLevel</a> function must be called before calling 
<b>MsiSetFeatureState</b>.

When <b>MsiSetFeatureState</b> is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state. However, there are common situations when the request cannot be fully implemented. For example, if a feature is tied to two components, component A and component B, through the <a href="/windows/desktop/Msi/featurecomponents-table">FeatureComponents</a> table, and component A has the <b>msidbComponentAttributesLocalOnly</b> attribute and component B has the <b>msidbComponentAttributesSourceOnly</b> attribute. In this case, if <b>MsiSetFeatureState</b> is called with a requested state of either INSTALLSTATE_LOCAL or INSTALLSTATE_SOURCE, the request cannot be fully implemented for both components. In this case, both components are turned ON, with component A set to Local and component B set to Source.

If more than one feature is linked to a single component (a common scenario), the final action state of that component is determined as follows:

<ul>
<li>If at least one feature requires the component to be installed locally, the feature is installed with a state of local.</li>
<li>If at least one feature requires the component to be run from the source, the feature is installed with a state of source.</li>
<li>If at least one feature requires the removal of the component, the action state is absent.</li>
</ul>
See 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions from Programs</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiSetFeatureState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Selection Functions</a>
