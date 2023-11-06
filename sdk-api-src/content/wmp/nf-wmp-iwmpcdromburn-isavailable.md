---
UID: NF:wmp.IWMPCdromBurn.isAvailable
title: IWMPCdromBurn::isAvailable (wmp.h)
description: The isAvailable method provides information about the CD drive and media.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","isAvailable method","IWMPCdromBurn.isAvailable","IWMPCdromBurn::isAvailable","IWMPCdromBurnisAvailable","isAvailable","isAvailable method [Windows Media Player]","isAvailable method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_isavailable","wmp/IWMPCdromBurn::isAvailable"]
old-location: wmp\iwmpcdromburn_isavailable.htm
tech.root: WMP
ms.assetid: 11876b73-10a1-49e2-ad45-33d9641c3647
ms.date: 4/26/2023
ms.keywords: IWMPCdromBurn interface [Windows Media Player],isAvailable method, IWMPCdromBurn.isAvailable, IWMPCdromBurn::isAvailable, IWMPCdromBurnisAvailable, isAvailable, isAvailable method [Windows Media Player], isAvailable method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_isavailable, wmp/IWMPCdromBurn::isAvailable
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn::isAvailable
 - wmp/IWMPCdromBurn::isAvailable
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
 - IWMPCdromBurn.isAvailable
---

# IWMPCdromBurn::isAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>isAvailable</b> method provides information about the CD drive and media.

## -parameters

### -param bstrItem [in]

<b>BSTR</b> that contains one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Burn</td>
<td>The drive is a CD burner.</td>
</tr>
<tr>
<td>Disc</td>
<td>There is a CD in the drive.</td>
</tr>
<tr>
<td>Erase</td>
<td>The CD can be erased.</td>
</tr>
<tr>
<td>Write</td>
<td>The CD can be written to.</td>
</tr>
</table>

### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates the result.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>