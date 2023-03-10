---
UID: NF:amparse.IAMParse.GetParseTime
title: IAMParse::GetParseTime (amparse.h)
description: The GetParseTime method retrieves the current stream parse time. For MPEG-2, this corresponds to the system clock time computed for the current stream position.
helpviewer_keywords: ["GetParseTime","GetParseTime method [DirectShow]","GetParseTime method [DirectShow]","IAMParse interface","IAMParse interface [DirectShow]","GetParseTime method","IAMParse.GetParseTime","IAMParse::GetParseTime","IAMParseGetParseTime","amparse/IAMParse::GetParseTime","dshow.iamparse_getparsetime"]
old-location: dshow\iamparse_getparsetime.htm
tech.root: dshow
ms.assetid: ce87e39e-1e5d-4098-8431-ea9b3188784e
ms.date: 12/05/2018
ms.keywords: GetParseTime, GetParseTime method [DirectShow], GetParseTime method [DirectShow],IAMParse interface, IAMParse interface [DirectShow],GetParseTime method, IAMParse.GetParseTime, IAMParse::GetParseTime, IAMParseGetParseTime, amparse/IAMParse::GetParseTime, dshow.iamparse_getparsetime
req.header: amparse.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMParse::GetParseTime
 - amparse/IAMParse::GetParseTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMParse.GetParseTime
---

# IAMParse::GetParseTime


## -description

The <code>GetParseTime</code> method retrieves the current stream parse time. For MPEG-2, this corresponds to the system clock time computed for the current stream position.

## -parameters

### -param prtCurrent [out]

Pointer to the current parse time.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The parse time is not available, because the input pin is not connected

</td>
</tr>
</table>

## -remarks

The parse time for the MPEG-2 Splitter filter is the current stream position in system clock units. The initial value of the parse time is zero.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amparse/nn-amparse-iamparse">IAMParse Interface</a>