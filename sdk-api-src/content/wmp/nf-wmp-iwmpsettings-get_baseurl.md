---
UID: NF:wmp.IWMPSettings.get_baseURL
title: IWMPSettings::get_baseURL (wmp.h)
description: The get_baseURL method retrieves the base URL used for relative path resolution with URL script commands that are embedded in digital media content.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_baseURL method","IWMPSettings.get_baseURL","IWMPSettings::get_baseURL","IWMPSettingsget_baseURL","get_baseURL","get_baseURL method [Windows Media Player]","get_baseURL method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_baseurl","wmp/IWMPSettings::get_baseURL"]
old-location: wmp\iwmpsettings_get_baseurl.htm
tech.root: WMP
ms.assetid: 2e4a2696-624f-4c6f-8947-2fe0b457332c
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_baseURL method, IWMPSettings.get_baseURL, IWMPSettings::get_baseURL, IWMPSettingsget_baseURL, get_baseURL, get_baseURL method [Windows Media Player], get_baseURL method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_baseurl, wmp/IWMPSettings::get_baseURL
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSettings::get_baseURL
 - wmp/IWMPSettings::get_baseURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.get_baseURL
---

# IWMPSettings::get_baseURL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_baseURL</b> method retrieves the base URL used for relative path resolution with URL script commands that are embedded in digital media content.

## -parameters

### -param pbstrBaseURL [out]

Pointer to a <b>BSTR</b> containing the base URL.

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

This method retrieves the base HTTP URL that is passed as the command parameter by the <b>ScriptCommand</b> event. The base URL is concatenated with the relative URL as follows:

1. A trailing forward slash (/) is added to the value retrieved by the <b>get_baseURL</b> method.
1. A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.
1. The relative URL is added to the end of the base URL.
1. All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.

> [!NOTE]
> The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.

**Windows Media Player 10 Mobile:** This method always retrieves a `BSTR` containing an empty string.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">IWMPEvents::ScriptCommand</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_baseurl">IWMPSettings::put_baseURL</a>