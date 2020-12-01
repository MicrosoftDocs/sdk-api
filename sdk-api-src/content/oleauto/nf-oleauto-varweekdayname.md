---
UID: NF:oleauto.VarWeekdayName
title: VarWeekdayName function (oleauto.h)
description: Returns a string containing the localized name of the weekday.
helpviewer_keywords: ["VarWeekdayName","VarWeekdayName function [Automation]","_oa96_VarWeekdayName","automat.varweekdayname","oleauto/VarWeekdayName"]
old-location: automat\varweekdayname.htm
tech.root: automat
ms.assetid: 8bd00c31-9ebf-4342-a8c0-ef73f5b5c108
ms.date: 12/05/2018
ms.keywords: VarWeekdayName, VarWeekdayName function [Automation], _oa96_VarWeekdayName, automat.varweekdayname, oleauto/VarWeekdayName
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
 - VarWeekdayName
 - oleauto/VarWeekdayName
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
 - VarWeekdayName
---

# VarWeekdayName function


## -description

Returns a string containing the localized name of the weekday.

## -parameters

### -param iWeekday [in]

The day of the week.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system default

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
</table>

### -param fAbbrev [in]

If zero then the full (non-abbreviated) weekday name is used. If non-zero, then the abbreviation for the weekday name is used.

### -param iFirstDay [in]

First day of the week.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system default

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
</table>

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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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

