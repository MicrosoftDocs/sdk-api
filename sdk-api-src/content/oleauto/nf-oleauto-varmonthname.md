---
UID: NF:oleauto.VarMonthName
title: VarMonthName function (oleauto.h)
description: Returns a string containing the localized month name.
helpviewer_keywords: ["VarMonthName","VarMonthName function [Automation]","_oa96_VarMonthName","automat.varmonthname","oleauto/VarMonthName"]
old-location: automat\varmonthname.htm
tech.root: automat
ms.assetid: 8bb760ae-2306-4c32-805d-58e5402e6d78
ms.date: 12/05/2018
ms.keywords: VarMonthName, VarMonthName function [Automation], _oa96_VarMonthName, automat.varmonthname, oleauto/VarMonthName
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarMonthName
 - oleauto/VarMonthName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarMonthName
---

# VarMonthName function


## -description

Returns a string containing the localized month name.

## -parameters

### -param iMonth [in]

Represents the month, as a number from 1 to 12.

### -param fAbbrev [in]

If zero then the full (non-abbreviated) month name is used. If non-zero, then the abbreviation for the month name is used.

### -param dwFlags [in]

VAR_CALENDAR_HIJRI is the only flag that can be set.

### -param pbstrOut [out]

Receives the formatted string that represents the variant.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
</table>

