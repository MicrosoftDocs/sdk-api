---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiEnumPatchesW function


## -description


The 
<b>MsiEnumPatches</b> function enumerates all of the patches that have been applied to a product. The function returns the patch code GUID for each patch that has been applied to the product and returns a list of transforms from each patch that apply to the product. Note that patches may have many transforms only some of which are applicable to a particular product. The list of transforms are returned in the same format as the value of the 
<a href="https://msdn.microsoft.com/da20f99e-3022-4382-97bb-8f1206072347">TRANSFORMS</a> property.
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



