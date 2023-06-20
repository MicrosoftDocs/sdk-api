---
UID: NF:wmp.IWMPDVD.get_isAvailable
title: IWMPDVD::get_isAvailable (wmp.h)
description: The get_isAvailable method indicates whether a specified type of information is available or a specified action can be performed.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","get_isAvailable method","IWMPDVD.get_isAvailable","IWMPDVD::get_isAvailable","IWMPDVDget_isAvailable","get_isAvailable","get_isAvailable method [Windows Media Player]","get_isAvailable method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_get_isavailable","wmp/IWMPDVD::get_isAvailable"]
old-location: wmp\iwmpdvd_get_isavailable.htm
tech.root: WMP
ms.assetid: bc8ce504-c387-4e3b-a227-926ae26ea78b
ms.date: 4/26/2023
ms.keywords: IWMPDVD interface [Windows Media Player],get_isAvailable method, IWMPDVD.get_isAvailable, IWMPDVD::get_isAvailable, IWMPDVDget_isAvailable, get_isAvailable, get_isAvailable method [Windows Media Player], get_isAvailable method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_get_isavailable, wmp/IWMPDVD::get_isAvailable
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
 - IWMPDVD::get_isAvailable
 - wmp/IWMPDVD::get_isAvailable
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
 - IWMPDVD.get_isAvailable
---

# IWMPDVD::get_isAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_isAvailable</b> method indicates whether a specified type of information is available or a specified action can be performed.

## -parameters

### -param bstrItem [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>back</td>
<td>Determines whether the <b>IWMPDVD::back</b> method is available.</td>
</tr>
<tr>
<td>dvd</td>
<td>Determines whether the DVD is loaded.</td>
</tr>
<tr>
<td>dvdDecoder</td>
<td>Determines whether the DVD decoder is installed on system.</td>
</tr>
<tr>
<td>resume</td>
<td>Determines whether the <b>IWMPDVD::resume</b> method is available.</td>
</tr>
<tr>
<td>titleMenu</td>
<td>Determines whether the <b>IWMPDVD::titleMenu</b> method is available.</td>
</tr>
<tr>
<td>topMenu</td>
<td>Determines whether the <b>IWMPDVD::topMenu</b> method is available. Commonly called the root menu.</td>
</tr>
</table>

### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the specified parameter is available.

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

The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed. You can determine whether a decoder is available by calling the <b>get_isAvailable</b> method and passing in the <b>BSTR</b> value "dvdDecoder".

Every DVD is authored differently. The methods available during DVD playback and navigation depend on how the DVD is authored.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-back">IWMPDVD::back</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-resume">IWMPDVD::resume</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-titlemenu">IWMPDVD::titleMenu</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-topmenu">IWMPDVD::topMenu</a>