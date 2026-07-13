---
UID: NF:mfobjects.IMFMediaBuffer.Unlock
title: IMFMediaBuffer::Unlock (mfobjects.h)
description: Unlocks a buffer that was previously locked. Call this method once for every call to IMFMediaBuffer::Lock.
helpviewer_keywords: ["3ca53321-5533-45f0-b415-6a16f780ec54","IMFMediaBuffer interface [Media Foundation]","Unlock method","IMFMediaBuffer.Unlock","IMFMediaBuffer::Unlock","Unlock","Unlock method [Media Foundation]","Unlock method [Media Foundation]","IMFMediaBuffer interface","mf.imfmediabuffer_unlock","mfobjects/IMFMediaBuffer::Unlock"]
old-location: mf\imfmediabuffer_unlock.htm
tech.root: mf
ms.assetid: 3ca53321-5533-45f0-b415-6a16f780ec54
ms.date: 12/05/2018
ms.keywords: 3ca53321-5533-45f0-b415-6a16f780ec54, IMFMediaBuffer interface [Media Foundation],Unlock method, IMFMediaBuffer.Unlock, IMFMediaBuffer::Unlock, Unlock, Unlock method [Media Foundation], Unlock method [Media Foundation],IMFMediaBuffer interface, mf.imfmediabuffer_unlock, mfobjects/IMFMediaBuffer::Unlock
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaBuffer::Unlock
 - mfobjects/IMFMediaBuffer::Unlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaBuffer.Unlock
---

# IMFMediaBuffer::Unlock


## -description

Unlocks a buffer that was previously locked. Call this method once for every call to <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a>.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
For Direct3D surface buffers, an error occurred when unlocking the surface.

</td>
</tr>
</table>

## -remarks

It is an error to call <b>Unlock</b> if you did not call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">Lock</a> previously.

After calling this method, do not use the pointer returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">Lock</a> method. It is no longer guaranteed to be valid.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>
