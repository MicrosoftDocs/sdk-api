---
UID: NF:oleauto.VarUdateFromDate
title: VarUdateFromDate function (oleauto.h)
description: Converts a time and date converted from variant format to MS-DOS format.
helpviewer_keywords: ["VarUdateFromDate","VarUdateFromDate function [Automation]","_oa96_VarUdateFromDate","automat.varudatefromdate","oleauto/VarUdateFromDate"]
old-location: automat\varudatefromdate.htm
tech.root: automat
ms.assetid: 59cd5573-db87-48ac-bc8e-7108b9a3b509
ms.date: 12/05/2018
ms.keywords: VarUdateFromDate, VarUdateFromDate function [Automation], _oa96_VarUdateFromDate, automat.varudatefromdate, oleauto/VarUdateFromDate
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
 - VarUdateFromDate
 - oleauto/VarUdateFromDate
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
 - VarUdateFromDate
---

# VarUdateFromDate function


## -description

Converts a time and date converted from variant format to MS-DOS format.

## -parameters

### -param dateIn [in]

The packed date.

### -param dwFlags [in]

Set for alternative calendars such as Hijri, Polish and Russian.

### -param pudateOut [out]

The unpacked date.

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
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The UDATE structure is used with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vardatefromudate">VarDateFromUdate</a> and <b>VarUdateFromDate</b>.  It represents an "unpacked" date.


``` syntax
typedef struct {
    SYSTEMTIME st;
    USHORT  wDayOfYear;
} UDATE;
```

The <b>VarUdateFromDate</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.
