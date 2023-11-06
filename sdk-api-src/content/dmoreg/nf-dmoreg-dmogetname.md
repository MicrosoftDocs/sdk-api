---
UID: NF:dmoreg.DMOGetName
title: DMOGetName function (dmoreg.h)
description: The DMOGetName function retrieves the name of a DMO from the registry.
helpviewer_keywords: ["DMOGetName","DMOGetName function [DirectShow]","dmoreg/DMOGetName","dshow.dmogetname"]
old-location: dshow\dmogetname.htm
tech.root: dshow
ms.assetid: 7cb803c2-4fe1-46e3-868d-1b7c28b07a5b
ms.date: 4/26/2023
ms.keywords: DMOGetName, DMOGetName function [DirectShow], dmoreg/DMOGetName, dshow.dmogetname
req.header: dmoreg.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMOGetName
 - dmoreg/DMOGetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - DMOGetName
---

# DMOGetName function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DMOGetName</b> function retrieves the name of a DMO from the registry.

## -parameters

### -param clsidDMO

Class identifier (CLSID) of the DMO.

### -param szName

Array of 80 Unicode characters that receives the name of the DMO. The caller must allocate the array. The name is a NULL-terminated string.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No name was registered for this DMO, or the name has zero length.

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

## -remarks

If the method returns S_FALSE, <i>szName</i> is set to '\0'.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-functions">DMO Functions</a>