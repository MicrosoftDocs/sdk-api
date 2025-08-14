---
UID: NF:msiquery.MsiGetComponentStateW
title: MsiGetComponentStateW function (msiquery.h)
description: The MsiGetComponentState function obtains the state of a component. (Unicode)
helpviewer_keywords: ["INSTALLSTATE_ABSENT", "INSTALLSTATE_DEFAULT", "INSTALLSTATE_LOCAL", "INSTALLSTATE_REMOVED", "INSTALLSTATE_SOURCE", "INSTALLSTATE_UNKNOWN", "MsiGetComponentState", "MsiGetComponentState function", "MsiGetComponentStateW", "_msi_msigetcomponentstate", "msiquery/MsiGetComponentState", "msiquery/MsiGetComponentStateW", "setup.msigetcomponentstate"]
old-location: setup\msigetcomponentstate.htm
tech.root: setup
ms.assetid: 343f5cbc-e026-4a51-9c54-da5d10b7caa8
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_REMOVED, INSTALLSTATE_SOURCE, INSTALLSTATE_UNKNOWN, MsiGetComponentState, MsiGetComponentState function, MsiGetComponentStateA, MsiGetComponentStateW, _msi_msigetcomponentstate, msiquery/MsiGetComponentState, msiquery/MsiGetComponentStateA, msiquery/MsiGetComponentStateW, setup.msigetcomponentstate
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetComponentStateW (Unicode) and MsiGetComponentStateA (ANSI)
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
 - MsiGetComponentStateW
 - msiquery/MsiGetComponentStateW
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
 - MsiGetComponentState
 - MsiGetComponentStateA
 - MsiGetComponentStateW
---

# MsiGetComponentStateW function


## -description

The 
<b>MsiGetComponentState</b> function obtains the state of a component.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szComponent [in]

A null-terminated string that specifies the component name within the product.

### -param piInstalled [out]

Receives the current installed state. This parameter must not be null. This parameter can be one of the following values. 



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
The component is not installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The component is installed in the default location: local or source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_REMOVED"></a><a id="installstate_removed"></a><dl>
<dt><b>INSTALLSTATE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The component is being removed. In action state and not settable.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component runs from the source, CD-ROM, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_UNKNOWN"></a><a id="installstate_unknown"></a><dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unrecognized product or feature name was passed to the function.

</td>
</tr>
</table>

### -param piAction [out]

Receives the action taken during the installation. This parameter must not be null. For return values, see <i>piInstalled</i>.

## -returns

The 
<b>MsiGetComponentState</b> function returns the following values:

## -remarks

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.

For more information, see 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.





> [!NOTE]
> The msiquery.h header defines MsiGetComponentState as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Selection Functions</a>



<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>
