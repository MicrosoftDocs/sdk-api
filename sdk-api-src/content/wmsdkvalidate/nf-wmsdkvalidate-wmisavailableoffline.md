---
UID: NF:wmsdkvalidate.WMIsAvailableOffline
title: WMIsAvailableOffline function (wmsdkvalidate.h)
description: The WMIsAvailableOffline function verifies that an ASF file can be played from a cached copy.
helpviewer_keywords: ["WMIsAvailableOffline","WMIsAvailableOffline function [windows Media Format]","wmformat.wmisavailableoffline","wmsdkvalidate/WMIsAvailableOffline"]
old-location: wmformat\wmisavailableoffline.htm
tech.root: wmformat
ms.assetid: caa700ba-143e-454b-9016-6e79c0a83271
ms.date: 4/26/2023
ms.keywords: WMIsAvailableOffline, WMIsAvailableOffline function [windows Media Format], wmformat.wmisavailableoffline, wmsdkvalidate/WMIsAvailableOffline
req.header: wmsdkvalidate.h
req.include-header: Wmsdkidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMIsAvailableOffline
 - wmsdkvalidate/WMIsAvailableOffline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMIsAvailableOffline
---

# WMIsAvailableOffline function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMIsAvailableOffline</b> function verifies that an ASF file can be played from a cached copy. If a user plays a file from a network location, part or all of the file may be stored in a cache. If that cached copy exists on the local machine, the user may be able to play the file without being connected to the network.

## -parameters

### -param pwszURL [in]

Wide-character <b>null</b>-terminated string containing the URL of the file to be checked.

### -param pwszLanguage [in]

Wide-character <b>null</b>-terminated string containing the RFC 1766-compliant language ID specifying which language is desired for playback. This value is only important for files that contain language-based mutual exclusion.

Set to <b>NULL</b> if all languages are acceptable.

### -param pfIsAvailableOffline [out]

Pointer to a Boolean value that is set to True if the file is available offline.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the input parameters are <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>