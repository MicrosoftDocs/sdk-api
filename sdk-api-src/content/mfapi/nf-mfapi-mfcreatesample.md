---
UID: NF:mfapi.MFCreateSample
title: MFCreateSample function (mfapi.h)
description: Creates an empty media sample.
helpviewer_keywords: ["MFCreateSample","MFCreateSample function [Media Foundation]","b8bc29a5-e872-4c7b-ad1d-6c6085aa1984","mf.mfcreatesample","mfapi/MFCreateSample"]
old-location: mf\mfcreatesample.htm
tech.root: mf
ms.assetid: b8bc29a5-e872-4c7b-ad1d-6c6085aa1984
ms.date: 12/05/2018
ms.keywords: MFCreateSample, MFCreateSample function [Media Foundation], b8bc29a5-e872-4c7b-ad1d-6c6085aa1984, mf.mfcreatesample, mfapi/MFCreateSample
req.header: mfapi.h
req.include-header: 
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSample
 - mfapi/MFCreateSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateSample
---

# MFCreateSample function


## -description

Creates an empty media sample.

## -parameters

### -param ppIMFSample

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the media sample. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>

## -remarks

Initially the sample does not contain any media buffers.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>