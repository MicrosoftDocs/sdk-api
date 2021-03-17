---
UID: NF:msctf.ITfContextOwnerServices.CreateRange
title: ITfContextOwnerServices::CreateRange (msctf.h)
description: The ITfContextOwnerServices::CreateRange method creates a new ranged based upon a specified character position.
helpviewer_keywords: ["CreateRange","CreateRange method [Text Services Framework]","CreateRange method [Text Services Framework]","ITfContextOwnerServices interface","ITfContextOwnerServices interface [Text Services Framework]","CreateRange method","ITfContextOwnerServices.CreateRange","ITfContextOwnerServices::CreateRange","_tsf_itfcontextownerservices_createrange_ref","msctf/ITfContextOwnerServices::CreateRange","tsf.itfcontextownerservices_createrange"]
old-location: tsf\itfcontextownerservices_createrange.htm
tech.root: TSF
ms.assetid: 60214fdb-212c-4967-8cbf-e988db893245
ms.date: 12/05/2018
ms.keywords: CreateRange, CreateRange method [Text Services Framework], CreateRange method [Text Services Framework],ITfContextOwnerServices interface, ITfContextOwnerServices interface [Text Services Framework],CreateRange method, ITfContextOwnerServices.CreateRange, ITfContextOwnerServices::CreateRange, _tsf_itfcontextownerservices_createrange_ref, msctf/ITfContextOwnerServices::CreateRange, tsf.itfcontextownerservices_createrange
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerServices::CreateRange
 - msctf/ITfContextOwnerServices::CreateRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerServices.CreateRange
---

# ITfContextOwnerServices::CreateRange


## -description

The <b>ITfContextOwnerServices::CreateRange</b> method creates a new ranged based upon a specified character position.

## -parameters

### -param acpStart [in]

Specifies the starting character position of the range.

### -param acpEnd [in]

Specifies the ending character position of the range.

### -param ppRange [out]

Receives a pointer to the range object within the specified starting and ending character positions.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified range is <b>NULL</b> or the specified starting character position is less than zero or the specified starting character position is greater than the specified ending character position.

</td>
</tr>
</table>

