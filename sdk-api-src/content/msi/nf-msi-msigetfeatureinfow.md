---
UID: NF:msi.MsiGetFeatureInfoW
title: MsiGetFeatureInfoW function (msi.h)
description: Returns descriptive information for a feature. (Unicode)
helpviewer_keywords: ["INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE", "INSTALLFEATUREATTRIBUTE_FAVORADVERTISE", "INSTALLFEATUREATTRIBUTE_FAVORLOCAL", "INSTALLFEATUREATTRIBUTE_FAVORSOURCE", "INSTALLFEATUREATTRIBUTE_FOLLOWPARENT", "INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE", "MsiGetFeatureInfo", "MsiGetFeatureInfo function", "MsiGetFeatureInfoW", "_msi_msigetfeatureinfo", "msi/MsiGetFeatureInfo", "msi/MsiGetFeatureInfoW", "setup.msigetfeatureinfo"]
old-location: setup\msigetfeatureinfo.htm
tech.root: setup
ms.assetid: 2553fddf-3349-4b48-86a9-be63f2d23684
ms.date: 12/05/2018
ms.keywords: INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE, INSTALLFEATUREATTRIBUTE_FAVORADVERTISE, INSTALLFEATUREATTRIBUTE_FAVORLOCAL, INSTALLFEATUREATTRIBUTE_FAVORSOURCE, INSTALLFEATUREATTRIBUTE_FOLLOWPARENT, INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE, MsiGetFeatureInfo, MsiGetFeatureInfo function, MsiGetFeatureInfoA, MsiGetFeatureInfoW, _msi_msigetfeatureinfo, msi/MsiGetFeatureInfo, msi/MsiGetFeatureInfoA, msi/MsiGetFeatureInfoW, setup.msigetfeatureinfo
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFeatureInfoW (Unicode) and MsiGetFeatureInfoA (ANSI)
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
 - MsiGetFeatureInfoW
 - msi/MsiGetFeatureInfoW
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
 - MsiGetFeatureInfo
 - MsiGetFeatureInfoA
 - MsiGetFeatureInfoW
---

# MsiGetFeatureInfoW function


## -description

The 
<b>MsiGetFeatureInfo</b> function returns descriptive information for a feature.

## -parameters

### -param hProduct [in]

Handle to the product that owns the feature. This handle is obtained from 
<a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szFeature [in]

Feature code for the feature about which information should be returned.

### -param lpAttributes [out, optional]

Pointer to a location containing one or more of the following Attribute flags. 





#### INSTALLFEATUREATTRIBUTE_FAVORLOCAL (1)



#### INSTALLFEATUREATTRIBUTE_FAVORSOURCE (2)



#### INSTALLFEATUREATTRIBUTE_FOLLOWPARENT (4)



#### INSTALLFEATUREATTRIBUTE_FAVORADVERTISE (8)



#### INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE (16)



#### INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE (32)

For more information, see  
<a href="/windows/desktop/Msi/feature-table">Feature Table</a>. The values that <b>MsiGetFeatureInfo</b> returns are double the values in the Attributes column of the Feature Table.

### -param lpTitleBuf [out, optional]

Pointer to a buffer to receive the localized name of the feature, which corresponds to the Title field in the <a href="/windows/desktop/Msi/feature-table">Feature Table</a>.

This parameter is optional and can be null.

### -param pcchTitleBuf [in, out, optional]

As input, the size of <i>lpTitleBuf</i>. As output, the number of characters returned in <i>lpTitleBuf</i>. On input, this is the full size of the buffer, and includes a space for a terminating null character. If the buffer that is passed in is too small, the count returned does not include the terminating null character.

### -param lpHelpBuf [out, optional]

Pointer to a buffer to receive the localized description of the feature, which corresponds to the Description field for the feature in the  <a href="/windows/desktop/Msi/feature-table">Feature table</a>.
This parameter is optional and can be null.

### -param pcchHelpBuf [in, out, optional]

As input, the size of <i>lpHelpBuf</i>. As output, the number of characters returned in <i>lpHelpBuf</i>. On input, this is the full size of the buffer, and includes a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE (16)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORADVERTISE (8)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORLOCAL (1)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FAVORSOURCE (2)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_FOLLOWPARENT (4)


##### - lpAttributes.INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE (32)

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The product handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function returns successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature is not known.

</td>
</tr>
</table>

## -remarks

The buffer sizes for the 
<b>MsiGetFeatureInfo</b> function should include an extra character for the terminating null character. If a buffer is too small, the returned string is truncated with null, and the buffer size contains the number of characters in the whole string, not including the terminating null character. For more information, see 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.





> [!NOTE]
> The msi.h header defines MsiGetFeatureInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Product Query Functions</a>
