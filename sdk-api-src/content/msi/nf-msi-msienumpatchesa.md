---
UID: NF:msi.MsiEnumPatchesA
title: MsiEnumPatchesA function (msi.h)
description: The MsiEnumPatches function enumerates all of the patches that have been applied to a product. (ANSI)
helpviewer_keywords: ["MsiEnumPatchesA", "msi/MsiEnumPatchesA"]
old-location: setup\msienumpatches.htm
tech.root: setup
ms.assetid: 8f15accf-1ff5-4aa3-8a8e-be0e339360d2
ms.date: 12/05/2018
ms.keywords: MsiEnumPatches, MsiEnumPatches function, MsiEnumPatchesA, MsiEnumPatchesW, _msi_msienumpatches, msi/MsiEnumPatches, msi/MsiEnumPatchesA, msi/MsiEnumPatchesW, setup.msienumpatches
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumPatchesW (Unicode) and MsiEnumPatchesA (ANSI)
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
 - MsiEnumPatchesA
 - msi/MsiEnumPatchesA
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
 - MsiEnumPatches
 - MsiEnumPatchesA
 - MsiEnumPatchesW
---

# MsiEnumPatchesA function


## -description

The 
<b>MsiEnumPatches</b> function enumerates all of the patches that have been applied to a product. The function returns the patch code GUID for each patch that has been applied to the product and returns a list of transforms from each patch that apply to the product. Note that patches may have many transforms only some of which are applicable to a particular product. The list of transforms are returned in the same format as the value of the 
<a href="/windows/desktop/Msi/transforms">TRANSFORMS</a> property.
<div class="alert"><b>Note</b>  <i>pcchTransformsBuf</i> is not set to the number of characters copied to <i>lpTransformsBuf</i> upon a successful return of 
<b>MsiEnumPatches</b>.</div><div> </div>

## -parameters

### -param szProduct [in]

Specifies the product code of the product for which patches are to be enumerated.

### -param iPatchIndex [in]

Specifies the index of the patch to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumPatches</b> function and then incremented for subsequent calls.

### -param lpPatchBuf [out]

Pointer to a buffer that receives the patch's GUID. This argument is required.

### -param lpTransformsBuf [out]

Pointer to a buffer that receives the list of transforms in the patch that are applicable to the product. This argument is required and cannot be Null.

### -param pcchTransformsBuf [in, out]

Set to the number of characters copied to <i>lpTransformsBuf</i> upon an unsuccessful return of the function. Not set for a successful return. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no patches to return.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
</table>

## -remarks

To enumerate patches, an application should initially call the 
<b>MsiEnumPatches</b> function with the <i>iPatchIndex</i> parameter set to zero. The application should then increment the <i>iPatchIndex</i> parameter and call 
<b>MsiEnumPatches</b> until there are no more products (until the function returns ERROR_NO_MORE_ITEMS).

If the buffer is too small to hold the requested data, 
<b>MsiEnumPatches</b> returns ERROR_MORE_DATA and <i>pcchTransformsBuf</i> contains the number of characters copied to <i>lpTransformsBuf</i>, without counting the Null character.




> [!NOTE]
> The msi.h header defines MsiEnumPatches as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
