---
UID: NF:sbe.IStreamBufferSink2.UnlockProfile
title: IStreamBufferSink2::UnlockProfile (sbe.h)
description: The UnlockProfile method unlocks the Stream Buffer Sink filter's profile. After the profile is unlocked, you can change the name of the stub file.
helpviewer_keywords: ["IStreamBufferSink2 interface [Microsoft TV Technologies]","UnlockProfile method","IStreamBufferSink2.UnlockProfile","IStreamBufferSink2::UnlockProfile","IStreamBufferSink2UnlockProfile","UnlockProfile","UnlockProfile method [Microsoft TV Technologies]","UnlockProfile method [Microsoft TV Technologies]","IStreamBufferSink2 interface","mstv.istreambuffersink2_unlockprofile","sbe/IStreamBufferSink2::UnlockProfile"]
old-location: mstv\istreambuffersink2_unlockprofile.htm
tech.root: mstv
ms.assetid: 71214ca2-2613-4dbe-a72b-37d4f768ab6b
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink2 interface [Microsoft TV Technologies],UnlockProfile method, IStreamBufferSink2.UnlockProfile, IStreamBufferSink2::UnlockProfile, IStreamBufferSink2UnlockProfile, UnlockProfile, UnlockProfile method [Microsoft TV Technologies], UnlockProfile method [Microsoft TV Technologies],IStreamBufferSink2 interface, mstv.istreambuffersink2_unlockprofile, sbe/IStreamBufferSink2::UnlockProfile
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IStreamBufferSink2::UnlockProfile
 - sbe/IStreamBufferSink2::UnlockProfile
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
 - IStreamBufferSink2.UnlockProfile
---

# IStreamBufferSink2::UnlockProfile


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>UnlockProfile</b> method unlocks the Stream Buffer Sink filter's profile. After the profile is unlocked, you can change the name of the stub file.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The profile is not currently locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The filter graph must be stopped when you call this method. If the recording session has not been started, this method invalidates the recording. To re-create the recording, call <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-lockprofile">IStreamBufferSink::LockProfile</a> again. If the profile is not already locked, the <b>UnlockProfile</b> method has no effect and returns S_FALSE.

If the graph is running, stopping the graph automatically unlocks the profile without the need to call <b>UnlockProfile</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink2">IStreamBufferSink2 Interface</a>
