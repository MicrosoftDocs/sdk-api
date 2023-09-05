---
UID: NF:sbe.IStreamBufferSink.IsProfileLocked
title: IStreamBufferSink::IsProfileLocked (sbe.h)
description: This topic applies only to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["IStreamBufferSink interface [Microsoft TV Technologies]","IsProfileLocked method","IStreamBufferSink.IsProfileLocked","IStreamBufferSink::IsProfileLocked","IStreamBufferSinkIsProfileLocked","IsProfileLocked","IsProfileLocked method [Microsoft TV Technologies]","IsProfileLocked method [Microsoft TV Technologies]","IStreamBufferSink interface","mstv.istreambuffersink_isprofilelocked","sbe/IStreamBufferSink::IsProfileLocked"]
old-location: mstv\istreambuffersink_isprofilelocked.htm
tech.root: mstv
ms.assetid: 941c1702-2ef2-4afe-933c-78ed9ee8690b
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink interface [Microsoft TV Technologies],IsProfileLocked method, IStreamBufferSink.IsProfileLocked, IStreamBufferSink::IsProfileLocked, IStreamBufferSinkIsProfileLocked, IsProfileLocked, IsProfileLocked method [Microsoft TV Technologies], IsProfileLocked method [Microsoft TV Technologies],IStreamBufferSink interface, mstv.istreambuffersink_isprofilelocked, sbe/IStreamBufferSink::IsProfileLocked
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferSink::IsProfileLocked
 - sbe/IStreamBufferSink::IsProfileLocked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSink.IsProfileLocked
---

# IStreamBufferSink::IsProfileLocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies only to Windows XP Service Pack 1 or later.
        



The <b>IsProfileLocked</b> method queries whether the Stream Buffer Sink filter's profile is locked.



## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The profile is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The profile is not locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

When the filter's profile is locked, the number of streams and their media types are fixed. For more information, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-lockprofile">IStreamBufferSink::LockProfile</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink">IStreamBufferSink Interface</a>
