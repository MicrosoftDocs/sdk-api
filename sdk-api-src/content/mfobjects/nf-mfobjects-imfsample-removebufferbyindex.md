---
UID: NF:mfobjects.IMFSample.RemoveBufferByIndex
title: IMFSample::RemoveBufferByIndex (mfobjects.h)
description: Removes a buffer at a specified index from the sample.
helpviewer_keywords: ["IMFSample interface [Media Foundation]","RemoveBufferByIndex method","IMFSample.RemoveBufferByIndex","IMFSample::RemoveBufferByIndex","RemoveBufferByIndex","RemoveBufferByIndex method [Media Foundation]","RemoveBufferByIndex method [Media Foundation]","IMFSample interface","fc7b5a46-a127-4d75-a9a5-382d9d65a426","mf.imfsample_removebufferbyindex","mfobjects/IMFSample::RemoveBufferByIndex"]
old-location: mf\imfsample_removebufferbyindex.htm
tech.root: medfound
ms.assetid: fc7b5a46-a127-4d75-a9a5-382d9d65a426
ms.date: 12/05/2018
ms.keywords: IMFSample interface [Media Foundation],RemoveBufferByIndex method, IMFSample.RemoveBufferByIndex, IMFSample::RemoveBufferByIndex, RemoveBufferByIndex, RemoveBufferByIndex method [Media Foundation], RemoveBufferByIndex method [Media Foundation],IMFSample interface, fc7b5a46-a127-4d75-a9a5-382d9d65a426, mf.imfsample_removebufferbyindex, mfobjects/IMFSample::RemoveBufferByIndex
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
 - IMFSample::RemoveBufferByIndex
 - mfobjects/IMFSample::RemoveBufferByIndex
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
 - IMFSample.RemoveBufferByIndex
---

# IMFSample::RemoveBufferByIndex


## -description

Removes a buffer at a specified index from the sample.

## -parameters

### -param dwIndex [in]

Index of the buffer. To find the number of buffers in the sample, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount">IMFSample::GetBufferCount</a>. Buffers are indexed from zero.

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

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>