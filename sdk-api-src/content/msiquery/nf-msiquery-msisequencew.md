---
UID: NF:msiquery.MsiSequenceW
title: MsiSequenceW function (msiquery.h)
description: The MsiSequence function executes another action sequence, as described in the specified table. (Unicode)
helpviewer_keywords: ["MsiSequence", "MsiSequence function", "MsiSequenceW", "_msi_msisequence", "msiquery/MsiSequence", "msiquery/MsiSequenceW", "setup.msisequence"]
old-location: setup\msisequence.htm
tech.root: setup
ms.assetid: affb33ab-1b58-4d18-a908-8eaedb9ce1ca
ms.date: 12/05/2018
ms.keywords: MsiSequence, MsiSequence function, MsiSequenceA, MsiSequenceW, _msi_msisequence, msiquery/MsiSequence, msiquery/MsiSequenceA, msiquery/MsiSequenceW, setup.msisequence
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSequenceW (Unicode) and MsiSequenceA (ANSI)
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
 - MsiSequenceW
 - msiquery/MsiSequenceW
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
 - MsiSequence
 - MsiSequenceA
 - MsiSequenceW
---

# MsiSequenceW function


## -description

The 
<b>MsiSequence</b> function executes another action sequence, as described in the specified table.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szTable [in]

Specifies the name of the table containing the action sequence.

### -param iSequenceMode [in]

This parameter is currently unimplemented. It is reserved for future use and must be 0.

## -returns

This function returns UINT.

## -remarks

The 
<b>MsiSequence</b> function queries the specified table, ordering the actions by the numbers in the Sequence column. For each row retrieved, an action is executed, provided that any supplied condition expression does not evaluate to FALSE.

An action sequence containing any actions that update the system, such as the 
<a href="/windows/desktop/Msi/installfiles-action">InstallFiles</a> and 
<a href="/windows/desktop/Msi/writeregistryvalues-action">WriteRegistryValues</a> actions, cannot be run by calling 
<b>MsiSequence</b>. The exception to this rule is if 
<b>MsiSequence</b> is called from a custom action that is scheduled in the 
<a href="/windows/desktop/Msi/installexecutesequence-table">InstallExecuteSequence table</a> between the 
<a href="/windows/desktop/Msi/installinitialize-action">InstallInitialize</a> and 
<a href="/windows/desktop/Msi/installfinalize-action">InstallFinalize actions</a>. Actions that do not update the system, such as 
<a href="/windows/desktop/Msi/appsearch-action">AppSearch</a> or 
<a href="/windows/desktop/Msi/costinitialize-action">CostInitialize</a>, can be called.





> [!NOTE]
> The msiquery.h header defines MsiSequence as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Action Functions</a>
