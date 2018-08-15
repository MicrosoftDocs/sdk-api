---
UID: NF:oleauto.VarDateFromUdate
title: VarDateFromUdate function
author: windows-sdk-content
description: Converts a time and date converted from MS-DOS format to variant format.
old-location: automat\vardatefromudate.htm
old-project: automat
ms.assetid: 1c924ac5-b896-49e1-9ccf-825ac7a030c8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VarDateFromUdate, VarDateFromUdate function [Automation], _oa96_VarDateFromUdate, automat.vardatefromudate, oleauto/VarDateFromUdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarDateFromUdate
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarDateFromUdate function


## -description


Converts a time and date converted from MS-DOS format to variant format.


## -parameters




### -param pudateIn [in]

The unpacked date.


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



The UDATE structure is used with <b>VarDateFromUdate</b>, <a href="https://msdn.microsoft.com/eb6f52fe-3324-4ff2-afcd-854a3a8a20cb">VarDateFromUdateEx</a>, and <a href="https://msdn.microsoft.com/59cd5573-db87-48ac-bc8e-7108b9a3b509">VarUdateFromDate</a>.  It represents an unpacked date.

<pre class="syntax" xml:space="preserve"><code>typedef struct {
    SYSTEMTIME st;
    USHORT  wDayOfYear;
} UDATE;</code></pre>
The <b>VarDateFromUdate</b> function will accept invalid dates and try to fix them when resolving to a VARIANT time. For example, an invalid date such as 2/29/2001 will resolve to 3/1/2001. Only days are fixed, so invalid month values result in an error being returned. Days are checked to be between 1 and 31. Negative days and days greater than 31 results in an error. A day less than 31 but greater than the maximum day in that month has the day promoted to the appropriate day of the next month. A day equal to zero resolves as the last day of the previous month. For example, an invalid dates such as 2/0/2001 will resolve to 1/31/2001.

Calling <b>VarDateFromUdate</b> has the same effect as calling <a href="https://msdn.microsoft.com/eb6f52fe-3324-4ff2-afcd-854a3a8a20cb">VarDateFromUdateEx</a> with the LCID 0x0409.



