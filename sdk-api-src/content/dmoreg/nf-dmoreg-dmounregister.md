---
UID: NF:dmoreg.DMOUnregister
title: DMOUnregister function (dmoreg.h)
description: The DMOUnregister function unregisters a DMO.
helpviewer_keywords: ["DMOUnregister","DMOUnregister function [DirectShow]","dmoreg/DMOUnregister","dshow.dmounregister"]
old-location: dshow\dmounregister.htm
tech.root: dshow
ms.assetid: 7f65789d-7654-4da2-a572-e07c1e81b4ae
ms.date: 4/26/2023
ms.keywords: DMOUnregister, DMOUnregister function [DirectShow], dmoreg/DMOUnregister, dshow.dmounregister
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
 - DMOUnregister
 - dmoreg/DMOUnregister
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
 - DMOUnregister
---

# DMOUnregister function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The DMOUnregister function unregisters a DMO.

## -parameters

### -param clsidDMO

Class identifier (CLSID) of the DMO.

### -param guidCategory

GUID that specifies the category from which to remove the DMO. Use GUID_NULL to unregister the DMO from every category. See <a href="/windows/desktop/DirectShow/dmo-guids">DMO GUIDs</a> for a list of category GUIDs.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Result Code</th>
<th>Description</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>This CLSID was not registered in the specified category.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dmo-functions">DMO Functions</a>