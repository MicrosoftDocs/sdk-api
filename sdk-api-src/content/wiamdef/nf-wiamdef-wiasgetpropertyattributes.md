---
UID: NF:wiamdef.wiasGetPropertyAttributes
title: wiasGetPropertyAttributes function
author: windows-driver-content
description: The wiasGetPropertyAttributes function retrieves the access flags and valid values for a set of properties.
old-location: image\wiasgetpropertyattributes.htm
old-project: image
ms.assetid: b12ff158-73e7-4fdf-b7b1-2969d161ed93
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetpropertyattributes, wiamdef/wiasGetPropertyAttributes, wiasFncs_d1a6ee77-54bc-400f-a670-e39889c71835.xml, wiasGetPropertyAttributes, wiasGetPropertyAttributes function [Imaging Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasGetPropertyAttributes
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetPropertyAttributes function


## -description


The <b>wiasGetPropertyAttributes </b>function retrieves the access flags and valid values for a set of properties.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param cPropSpec

Specifies the number of properties.


### -param pPropSpec [in]

Pointer to a PROPSPEC structure (defined in the Microsoft Windows SDK documentation) indicating the properties for which to get valid values and access flags.


### -param pulAccessFlags

Pointer to an array that contains the access flags for the properties.


### -param pPropVar [out]

Pointer to an array of PROPVARIANT structures (defined in the Microsoft Windows SDK documentation) that contains the valid values for the properties.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Windows SDK documentation).




## -remarks



This function fills each element of the <i>pPropVar </i>array with a PROPVARIANT structure that specifies the valid values for the corresponding property. Properties with the access rights flag WIA_PROP_NONE have no valid values for that property. The data type for the valid values of these properties is VT_EMPTY.

One or more of the WIA_PROP_Xxx property attributes and access flags can be returned in each element of the <i>pulAccessFlags</i> array. The property attribute constants are described in the Windows SDK documentation.

If the property has a range of valid values, the values can be determined through the <i>pPropVar </i>parameter upon completion of this function. The <i>pPropVar </i>parameter specifies an array of PROPVARIANT structures.

Valid integer and floating-point values in a range are accessed using the following index constants.

<table>
<tr>
<th>Valid Value Index</th>
<th>Description</th>
</tr>
<tr>
<td>
WIA_RANGE_MIN  

</td>
<td>
Minimum value

</td>
</tr>
<tr>
<td>
WIA_RANGE_NOM  

</td>
<td>
Nominal value

</td>
</tr>
<tr>
<td>
WIA_RANGE_MAX  

</td>
<td>
Maximum value

</td>
</tr>
<tr>
<td>
WIA_RANGE_STEP

</td>
<td>
Increment value

</td>
</tr>
</table>
 

Valid list values are accessed using the following index constants.

<table>
<tr>
<th>Valid Value Index</th>
<th>Description</th>
</tr>
<tr>
<td>
WIA_LIST_COUNT

</td>
<td>
Count of valid list values, not counting the nominal value

</td>
</tr>
<tr>
<td>
WIA_LIST_NOM

</td>
<td>
Nominal value

</td>
</tr>
<tr>
<td>
WIA_LIST_VALUES

</td>
<td>
Index to first valid value

</td>
</tr>
</table>
 

Valid bitwise flag values are accessed using the following index constants.

<table>
<tr>
<th>Valid Value Index</th>
<th>Description</th>
</tr>
<tr>
<td>
WIA_FLAG_NOM   

</td>
<td>
Nominal value

</td>
</tr>
<tr>
<td>
WIA_FLAG_VALUES

</td>
<td>
All valid flags are joined together by an OR operator

</td>
</tr>
</table>
 

The PROPSPEC and PROPVARIANT structures are defined in the Microsoft Windows SDK documentation.



