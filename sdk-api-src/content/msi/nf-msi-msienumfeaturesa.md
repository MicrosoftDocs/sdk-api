---
UID: NF:msi.MsiEnumFeaturesA
title: MsiEnumFeaturesA function (msi.h)
description: The MsiEnumFeatures function enumerates the published features for a given product. This function retrieves one feature ID each time it is called. (ANSI)
helpviewer_keywords: ["MsiEnumFeaturesA", "msi/MsiEnumFeaturesA"]
old-location: setup\msienumfeatures.htm
tech.root: setup
ms.assetid: 0ac6fea4-cdc8-4799-9001-f9399b22e7a5
ms.date: 12/05/2018
ms.keywords: MsiEnumFeatures, MsiEnumFeatures function, MsiEnumFeaturesA, MsiEnumFeaturesW, _msi_msienumfeatures, msi/MsiEnumFeatures, msi/MsiEnumFeaturesA, msi/MsiEnumFeaturesW, setup.msienumfeatures
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumFeaturesW (Unicode) and MsiEnumFeaturesA (ANSI)
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
 - MsiEnumFeaturesA
 - msi/MsiEnumFeaturesA
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
 - MsiEnumFeatures
 - MsiEnumFeaturesA
 - MsiEnumFeaturesW
---

# MsiEnumFeaturesA function


## -description

The 
<b>MsiEnumFeatures</b> function enumerates the published features for a given product. This function retrieves one feature ID each time it is called.

## -parameters

### -param szProduct [in]

Null-terminated string specifying the product code of the product whose features are to be enumerated.

### -param iFeatureIndex [in]

Specifies the index of the feature to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumFeatures</b> function and then incremented for subsequent calls. Because features are not ordered, any new feature has an arbitrary index. This means that the function can return features in any order.

### -param lpFeatureBuf [out]

Pointer to a buffer that receives the feature ID. The size of the buffer must hold a string value of length MAX_FEATURE_CHARS+1.  The function returns <b>ERROR_MORE_DATA</b> if the length of the feature ID exceeds <b>MAX_FEATURE_CHARS</b>.

### -param lpParentBuf [out]

Pointer to a buffer that receives the feature ID of the parent of the feature. The size of the buffer must hold a string value of length MAX_FEATURE_CHARS+1.  If the length of the feature ID of the parent feature exceeds <b>MAX_FEATURE_CHARS</b>, only the first <b>MAX_FEATURE_CHARS</b> characters get copied into the buffer.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no features to return.

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
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The specified product is unknown.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

To enumerate features, an application should initially call the 
<b>MsiEnumFeatures</b> function with the <i>iFeatureIndex</i> parameter set to zero. The application should then increment the <i>iFeatureIndex</i> parameter and call 
<b>MsiEnumFeatures</b> until there are no more features (that is, until the function returns ERROR_NO_MORE_ITEMS).





> [!NOTE]
> The msi.h header defines MsiEnumFeatures as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
