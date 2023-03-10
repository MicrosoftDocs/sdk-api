---
UID: NF:oleauto.VarDateFromUdateEx
title: VarDateFromUdateEx function (oleauto.h)
description: Converts a time and date converted from MS-DOS format to variant format. (VarDateFromUdateEx)
helpviewer_keywords: ["VarDateFromUdateEx","VarDateFromUdateEx function [Automation]","_oa96_VarDateFromUdateEx","automat.vardatefromudateex","oleauto/VarDateFromUdateEx"]
old-location: automat\vardatefromudateex.htm
tech.root: automat
ms.assetid: eb6f52fe-3324-4ff2-afcd-854a3a8a20cb
ms.date: 12/05/2018
ms.keywords: VarDateFromUdateEx, VarDateFromUdateEx function [Automation], _oa96_VarDateFromUdateEx, automat.vardatefromudateex, oleauto/VarDateFromUdateEx
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
 - VarDateFromUdateEx
 - oleauto/VarDateFromUdateEx
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
 - VarDateFromUdateEx
---

# VarDateFromUdateEx function


## -description

Converts a time and date converted from MS-DOS format to variant format.

## -parameters

### -param pudateIn [in]

The unpacked date.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

VAR_VALIDDATE if the date is valid.

### -param pdateOut [out]

The packed date.

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

The UDATE structure is used with <b>VarDateFromUdateEx</b>, <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vardatefromudate">VarDateFromUdate</a>, and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varudatefromdate">VarUdateFromDate</a>.  It represents an unpacked date.


``` syntax
typedef struct {
    SYSTEMTIME st;
    USHORT  wDayOfYear;
} UDATE;
```

The <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vardatefromudate">VarDateFromUdate</a> function accepts invalid dates and tries to fix them when resolving to a VARIANT time. Only days are fixed, so invalid month values result in an error being returned. Days are checked to verify that they are in the range of 1 through 31. Negative days and days greater than 31 result in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. For example, an invalid date such as 2/29/2001 resolves to 3/1/2001. A day equal to zero resolves as the last day of the previous month. For example, an invalid date such as 2/0/2001 resolves to 1/31/2001.
