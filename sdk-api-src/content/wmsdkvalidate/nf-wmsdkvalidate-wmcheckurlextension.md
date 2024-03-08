---
UID: NF:wmsdkvalidate.WMCheckURLExtension
title: WMCheckURLExtension function (wmsdkvalidate.h)
description: The WMCheckURLExtension function examines the file name extension in the URL or file name that is passed in as an argument.
helpviewer_keywords: ["WMCheckURLExtension","WMCheckURLExtension function [windows Media Format]","wmformat.wmcheckurlextension","wmsdkvalidate/WMCheckURLExtension"]
old-location: wmformat\wmcheckurlextension.htm
tech.root: wmformat
ms.assetid: f001d9e7-ccbd-4dc9-bb4b-fe45cb47700c
ms.date: 4/26/2023
ms.keywords: WMCheckURLExtension, WMCheckURLExtension function [windows Media Format], wmformat.wmcheckurlextension, wmsdkvalidate/WMCheckURLExtension
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
 - WMCheckURLExtension
 - wmsdkvalidate/WMCheckURLExtension
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
 - WMCheckURLExtension
---

# WMCheckURLExtension function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMCheckURLExtension</b> function examines the file name extension in the URL or file name that is passed in as an argument. The extension is compared to a list of supported file types in an attempt to determine whether the file can be opened by the objects of this SDK.



If you are writing an application that can handle many different file types, you can use this function to try to quickly determine whether the file can be read using objects of the Windows Media Format SDK.

## -parameters

### -param pwszURL [in]

A wide-character <b>null</b>-terminated string containing a file name or URL.

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
The function succeeded, and the file extension is supported. This result does not indicate verification of the contents of the file, just the extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The URL passed is not of a type supported by the objects of the Windows Media Format SDK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszURL</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This function cannot report with absolute certainty whether a particular URL can be handled, as this cannot be determined until the URL is opened.

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>