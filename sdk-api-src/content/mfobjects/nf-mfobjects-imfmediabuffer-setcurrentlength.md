---
UID: NF:mfobjects.IMFMediaBuffer.SetCurrentLength
title: IMFMediaBuffer::SetCurrentLength (mfobjects.h)
description: Sets the length of the valid data in the buffer.
helpviewer_keywords: ["IMFMediaBuffer interface [Media Foundation]","SetCurrentLength method","IMFMediaBuffer.SetCurrentLength","IMFMediaBuffer::SetCurrentLength","SetCurrentLength","SetCurrentLength method [Media Foundation]","SetCurrentLength method [Media Foundation]","IMFMediaBuffer interface","ce48458f-eb0f-441a-a4bc-9d3fbee0cd74","mf.imfmediabuffer_setcurrentlength","mfobjects/IMFMediaBuffer::SetCurrentLength"]
old-location: mf\imfmediabuffer_setcurrentlength.htm
tech.root: mf
ms.assetid: ce48458f-eb0f-441a-a4bc-9d3fbee0cd74
ms.date: 12/05/2018
ms.keywords: IMFMediaBuffer interface [Media Foundation],SetCurrentLength method, IMFMediaBuffer.SetCurrentLength, IMFMediaBuffer::SetCurrentLength, SetCurrentLength, SetCurrentLength method [Media Foundation], SetCurrentLength method [Media Foundation],IMFMediaBuffer interface, ce48458f-eb0f-441a-a4bc-9d3fbee0cd74, mf.imfmediabuffer_setcurrentlength, mfobjects/IMFMediaBuffer::SetCurrentLength
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
 - IMFMediaBuffer::SetCurrentLength
 - mfobjects/IMFMediaBuffer::SetCurrentLength
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
 - IMFMediaBuffer.SetCurrentLength
---

# IMFMediaBuffer::SetCurrentLength


## -description

Sets the length of the valid data in the buffer.

## -parameters

### -param cbCurrentLength [in]

Length of the valid data, in bytes. This value cannot be greater than the allocated size of the buffer, which is returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength">IMFMediaBuffer::GetMaxLength</a> method.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified length is greater than the maximum size of the buffer.

</td>
</tr>
</table>

## -remarks

Call this method if you write data into the buffer.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>