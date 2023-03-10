---
UID: NF:strmif.IAMClockSlave.GetErrorTolerance
title: IAMClockSlave::GetErrorTolerance (strmif.h)
description: The GetErrorTolerance method retrieves the audio renderer's rate-matching tolerance.
helpviewer_keywords: ["GetErrorTolerance","GetErrorTolerance method [DirectShow]","GetErrorTolerance method [DirectShow]","IAMClockSlave interface","IAMClockSlave interface [DirectShow]","GetErrorTolerance method","IAMClockSlave.GetErrorTolerance","IAMClockSlave::GetErrorTolerance","IAMClockSlaveGetErrorTolerance","dshow.iamclockslave_geterrortolerance","strmif/IAMClockSlave::GetErrorTolerance"]
old-location: dshow\iamclockslave_geterrortolerance.htm
tech.root: dshow
ms.assetid: a22e17d8-eb96-4e67-bbd7-7c116694c891
ms.date: 12/05/2018
ms.keywords: GetErrorTolerance, GetErrorTolerance method [DirectShow], GetErrorTolerance method [DirectShow],IAMClockSlave interface, IAMClockSlave interface [DirectShow],GetErrorTolerance method, IAMClockSlave.GetErrorTolerance, IAMClockSlave::GetErrorTolerance, IAMClockSlaveGetErrorTolerance, dshow.iamclockslave_geterrortolerance, strmif/IAMClockSlave::GetErrorTolerance
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IAMClockSlave::GetErrorTolerance
 - strmif/IAMClockSlave::GetErrorTolerance
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
 - IAMClockSlave.GetErrorTolerance
---

# IAMClockSlave::GetErrorTolerance


## -description

The <code>GetErrorTolerance</code> method retrieves the audio renderer's rate-matching tolerance.

## -parameters

### -param pdwTolerance [out]

Pointer to a variable that receives the maximum tolerance, in milliseconds.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamclockslave">IAMClockSlave Interface</a>