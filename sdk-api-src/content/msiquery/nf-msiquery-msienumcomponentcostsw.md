---
UID: NF:msiquery.MsiEnumComponentCostsW
title: MsiEnumComponentCostsW function (msiquery.h)
description: The MsiEnumComponentCosts function enumerates the disk-space per drive required to install a component. (Unicode)
helpviewer_keywords: ["MsiEnumComponentCosts", "MsiEnumComponentCosts function", "MsiEnumComponentCostsW", "_msi_msienumcomponentcosts", "msiquery/MsiEnumComponentCosts", "msiquery/MsiEnumComponentCostsW", "setup.msienumcomponentcosts"]
old-location: setup\msienumcomponentcosts.htm
tech.root: setup
ms.assetid: 3de3a044-2780-445b-a09f-f08ff82f91f3
ms.date: 12/05/2018
ms.keywords: MsiEnumComponentCosts, MsiEnumComponentCosts function, MsiEnumComponentCostsA, MsiEnumComponentCostsW, _msi_msienumcomponentcosts, msiquery/MsiEnumComponentCosts, msiquery/MsiEnumComponentCostsA, msiquery/MsiEnumComponentCostsW, setup.msienumcomponentcosts
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumComponentCostsW (Unicode) and MsiEnumComponentCostsA (ANSI)
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
 - MsiEnumComponentCostsW
 - msiquery/MsiEnumComponentCostsW
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
 - MsiEnumComponentCosts
 - MsiEnumComponentCostsA
 - MsiEnumComponentCostsW
---

# MsiEnumComponentCostsW function


## -description

The 
<b>MsiEnumComponentCosts</b> function enumerates the disk-space per drive required to install a component. This information is needed to display the disk-space cost required for all drives in the user interface. The returned disk-space costs are expressed in multiples of 512 bytes.

<b>MsiEnumComponentCosts</b> should only be run after the installer has completed file costing and after the 
<a href="/windows/desktop/Msi/costfinalize-action">CostFinalize action</a>. For more information, see 
<a href="/windows/desktop/Msi/file-costing">File Costing</a>.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szComponent [in]

A null-terminated string specifying the component's name as it is listed in the Component column of the 
<a href="/windows/desktop/Msi/component-table">Component table</a>. This parameter can be null. If <i>szComponent</i> is null or an empty string, 
<b>MsiEnumComponentCosts</b> enumerates the total disk-space per drive used during the installation. In this case, <i>iState</i> is ignored. The costs of the installer include those costs for caching the database in the secure folder as well as the cost to create the installation script. Note that the total disk-space used during the installation may be larger than the space used after the component is installed.

### -param dwIndex [in]

0-based index for drives. This parameter should be zero for the first call to the 
<b>MsiEnumComponentCosts</b> function and then incremented for subsequent calls.

### -param iState [in]

Requested component state to be enumerated. If <i>szComponent</i> is passed as Null or an empty string, the installer ignores the <i>iState</i> parameter.

### -param szDriveBuf [out]

Buffer that holds the drive name including the null terminator. This is an empty string in case of an error.

### -param pcchDriveBuf [in, out]

Pointer to a variable that specifies the size, in TCHARs, of the buffer pointed to by the <i>lpDriveBuf</i> parameter. This size should include the terminating null character. If the buffer provided is too small, the variable pointed to by <i>pcchDriveBuf</i> contains the count of characters not including the null terminator.

### -param piCost [out]

Cost of the component per drive expressed in multiples of 512 bytes. This value is 0 if an error has occurred. The value returned in <i>piCost</i> is final disk-space used by the component after installation. If <i>szComponent</i> is passed as Null or an empty string, the installer sets the value at <i>piCost</i> to 0.

### -param piTempCost [out]

The component cost per drive for the duration of the installation, or 0 if an error occurred. The value in *<i>piTempCost</i> represents the temporary space requirements for the duration of the installation. This temporary space requirement is space needed only for the duration of the installation. This does not affect the final disk space requirement.

## -returns

<table>
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more drives to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The component is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_NOT_CALLED</b></dt>
</dl>
</td>
<td width="60%">
Costing is not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Buffer not large enough for the drive name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The supplied handle is invalid or inactive.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The recommended method for enumerating the disk-space costs per drive is as follows. Start with the dwIndex set to 0 and increment it by one after each call. Continue the enumeration as long as 
<b>MsiEnumComponentCosts</b> returns ERROR_SUCCESS.

<b>MsiEnumComponentCosts</b> may be called from custom actions.

The total final disk cost for the installation is the sum of the costs of all components plus the cost of the Windows Installer (<i>szComponent</i> = null).




> [!NOTE]
> The msiquery.h header defines MsiEnumComponentCosts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
