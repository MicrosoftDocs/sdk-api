---
UID: NF:strmif.IDvdState.GetDiscID
title: IDvdState::GetDiscID (strmif.h)
description: The GetDiscID method retrieves the unique ID of the disc from which the bookmark was made.
helpviewer_keywords: ["GetDiscID","GetDiscID method [DirectShow]","GetDiscID method [DirectShow]","IDvdState interface","IDvdState interface [DirectShow]","GetDiscID method","IDvdState.GetDiscID","IDvdState::GetDiscID","IDvdStateGetDiscID","dshow.idvdstate_getdiscid","strmif/IDvdState::GetDiscID"]
old-location: dshow\idvdstate_getdiscid.htm
tech.root: dshow
ms.assetid: 1a3d8dba-4281-4385-b48f-d9d1b1134676
ms.date: 12/05/2018
ms.keywords: GetDiscID, GetDiscID method [DirectShow], GetDiscID method [DirectShow],IDvdState interface, IDvdState interface [DirectShow],GetDiscID method, IDvdState.GetDiscID, IDvdState::GetDiscID, IDvdStateGetDiscID, dshow.idvdstate_getdiscid, strmif/IDvdState::GetDiscID
req.header: strmif.h
req.include-header: Dshow.h
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
 - IDvdState::GetDiscID
 - strmif/IDvdState::GetDiscID
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
 - IDvdState.GetDiscID
---

# IDvdState::GetDiscID


## -description

The <code>GetDiscID</code> method retrieves the unique ID of the disc from which the bookmark was made.

## -parameters

### -param pullUniqueID [out]

Receives the ID.

## -returns

Returns one of the values shown in the following table.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdstate">IDvdState Interface</a>