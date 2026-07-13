---
UID: NF:msi.MsiLocateComponentA
title: MsiLocateComponentA function (msi.h)
description: The MsiLocateComponent function returns the full path to an installed component without a product code. (ANSI)
helpviewer_keywords: ["MsiLocateComponentA", "msi/MsiLocateComponentA"]
old-location: setup\msilocatecomponent.htm
tech.root: setup
ms.assetid: 5b6235c5-9a64-4b4e-9f2c-42ed73400cbe
ms.date: 12/05/2018
ms.keywords: MsiLocateComponent, MsiLocateComponent function, MsiLocateComponentA, MsiLocateComponentW, _msi_msilocatecomponent, msi/MsiLocateComponent, msi/MsiLocateComponentA, msi/MsiLocateComponentW, setup.msilocatecomponent
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiLocateComponentW (Unicode) and MsiLocateComponentA (ANSI)
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
 - MsiLocateComponentA
 - msi/MsiLocateComponentA
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
 - MsiLocateComponent
 - MsiLocateComponentA
 - MsiLocateComponentW
---

# MsiLocateComponentA function


## -description

The 
<b>MsiLocateComponent</b> function returns the full path to an installed component without a product code. This function attempts to determine the product using 
<a href="/windows/desktop/api/msi/nf-msi-msigetproductcodea">MsiGetProductCode</a>, but is not guaranteed to find the correct product for the caller. 
<a href="/windows/desktop/api/msi/nf-msi-msigetcomponentpatha">MsiGetComponentPath</a> should always be called when possible.

## -parameters

### -param szComponent [in]

Specifies the component ID of the component to be located.

### -param lpPathBuf [out]

Pointer to a variable that receives the path to the component. The variable includes the terminating null character.

### -param pcchBuf [in, out]

Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpPathBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. Upon success of the 
<b>MsiLocateComponent</b> function, the variable pointed to by <i>pcchBuf</i> contains the count of characters not including the terminating null character. If the size of the buffer passed in is too small, the function returns INSTALLSTATE_MOREDATA. 




If <i>lpPathBuf</i> is null, <i>pcchBuf</i> can be null.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_NOTUSED</b></dt>
</dl>
</td>
<td width="60%">
The component being requested is disabled on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component is not installed. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed locally.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer provided was too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component is installed to run from source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_SOURCEABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component source is inaccessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product code or component ID is unknown. See Remarks.

</td>
</tr>
</table>

## -remarks

The 
<b>MsiLocateComponent</b> function might return INSTALLSTATE_ABSENT or INSTALL_STATE_UNKNOWN, for the following reasons:

<ul>
<li>INSTALLSTATE_ABSENT 


The application did not properly ensure that the feature was installed by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a> and, if necessary, 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>.

</li>
<li>INSTALLSTATE_UNKNOWN 


The feature is not published. The application should have determined this earlier by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea">MsiQueryFeatureState</a> or 
<a href="/windows/desktop/api/msi/nf-msi-msienumfeaturesa">MsiEnumFeatures</a>. The application makes these calls while it initializes. An application should only use features that are known to be published. Since INSTALLSTATE_UNKNOWN should have been returned by 
<a href="/windows/desktop/api/msi/nf-msi-msiusefeaturea">MsiUseFeature</a> as well, either 
<b>MsiUseFeature</b> was not called, or its return value was not properly checked.

</li>
</ul>




> [!NOTE]
> The msi.h header defines MsiLocateComponent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Component-Specific Functions</a>
