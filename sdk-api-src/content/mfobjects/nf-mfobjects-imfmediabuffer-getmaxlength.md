---
UID: NF:mfobjects.IMFMediaBuffer.GetMaxLength
title: IMFMediaBuffer::GetMaxLength (mfobjects.h)
description: Retrieves the allocated size of the buffer.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [Media Foundation]","GetMaxLength method [Media Foundation]","IMFMediaBuffer interface","IMFMediaBuffer interface [Media Foundation]","GetMaxLength method","IMFMediaBuffer.GetMaxLength","IMFMediaBuffer::GetMaxLength","f0697f1d-18d6-4406-9f19-8cbaac08ad47","mf.imfmediabuffer_getmaxlength","mfobjects/IMFMediaBuffer::GetMaxLength"]
old-location: mf\imfmediabuffer_getmaxlength.htm
tech.root: mf
ms.assetid: f0697f1d-18d6-4406-9f19-8cbaac08ad47
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [Media Foundation], GetMaxLength method [Media Foundation],IMFMediaBuffer interface, IMFMediaBuffer interface [Media Foundation],GetMaxLength method, IMFMediaBuffer.GetMaxLength, IMFMediaBuffer::GetMaxLength, f0697f1d-18d6-4406-9f19-8cbaac08ad47, mf.imfmediabuffer_getmaxlength, mfobjects/IMFMediaBuffer::GetMaxLength
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
 - IMFMediaBuffer::GetMaxLength
 - mfobjects/IMFMediaBuffer::GetMaxLength
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
 - IMFMediaBuffer.GetMaxLength
---

# IMFMediaBuffer::GetMaxLength


## -description

Retrieves the allocated size of the buffer.

## -parameters

### -param pcbMaxLength [out]

Receives the allocated size of the buffer, in bytes.

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
</table>

## -remarks

The buffer might or might not contain any valid data, and if there is valid data in the buffer, it might be smaller than the buffer's allocated size. To get the length of the valid data, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>