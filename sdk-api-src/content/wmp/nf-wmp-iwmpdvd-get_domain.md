---
UID: NF:wmp.IWMPDVD.get_domain
title: IWMPDVD::get_domain (wmp.h)
description: The get_domain method retrieves the current domain of the DVD.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","get_domain method","IWMPDVD.get_domain","IWMPDVD::get_domain","IWMPDVDget_domain","get_domain","get_domain method [Windows Media Player]","get_domain method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_get_domain","wmp/IWMPDVD::get_domain"]
old-location: wmp\iwmpdvd_get_domain.htm
tech.root: WMP
ms.assetid: 2a8d5ea6-ed70-4952-810c-215acd1ae560
ms.date: 4/26/2023
ms.keywords: IWMPDVD interface [Windows Media Player],get_domain method, IWMPDVD.get_domain, IWMPDVD::get_domain, IWMPDVDget_domain, get_domain, get_domain method [Windows Media Player], get_domain method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_get_domain, wmp/IWMPDVD::get_domain
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMPDVD::get_domain
 - wmp/IWMPDVD::get_domain
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
 - IWMPDVD.get_domain
---

# IWMPDVD::get_domain


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_domain</b> method retrieves the current domain of the DVD.

## -parameters

### -param strDomain [out]

Pointer to a <b>BSTR</b> that contains one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>firstPlay</td>
<td>Performing default initialization of a DVD disc.</td>
</tr>
<tr>
<td>videoManagerMenu</td>
<td>Displaying menus for the entire disc. Also known as topMenu for Windows Media Player. Commonly called the title menu or the top menu.</td>
</tr>
<tr>
<td>videoTitleSetMenu</td>
<td>Displaying menus for current title set. Also known as titleMenu for Windows Media Player. Commonly called the root menu.</td>
</tr>
<tr>
<td>title</td>
<td>Usually displaying the current title.</td>
</tr>
<tr>
<td>stop</td>
<td>The DVD Navigator is in the DVD Stop domain.</td>
</tr>
<tr>
<td>undefined</td>
<td>Windows Media Player is not in any DVD domain.</td>
</tr>
</table>

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

Every DVD is authored differently. Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>