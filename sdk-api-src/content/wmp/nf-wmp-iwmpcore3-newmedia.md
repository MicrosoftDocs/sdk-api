---
UID: NF:wmp.IWMPCore3.newMedia
title: IWMPCore3::newMedia (wmp.h)
description: The newMedia method retrieves a pointer to an IWMPMedia interface for a new media item.
helpviewer_keywords: ["IWMPCore3 interface [Windows Media Player]","newMedia method","IWMPCore3.newMedia","IWMPCore3::newMedia","IWMPCore3newMedia","newMedia","newMedia method [Windows Media Player]","newMedia method [Windows Media Player]","IWMPCore3 interface","wmp.iwmpcore3_newmedia","wmp/IWMPCore3::newMedia"]
old-location: wmp\iwmpcore3_newmedia.htm
tech.root: WMP
ms.assetid: d0ae488f-cdc8-4688-bfc5-b7821216da37
ms.date: 4/26/2023
ms.keywords: IWMPCore3 interface [Windows Media Player],newMedia method, IWMPCore3.newMedia, IWMPCore3::newMedia, IWMPCore3newMedia, newMedia, newMedia method [Windows Media Player], newMedia method [Windows Media Player],IWMPCore3 interface, wmp.iwmpcore3_newmedia, wmp/IWMPCore3::newMedia
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
 - IWMPCore3::newMedia
 - wmp/IWMPCore3::newMedia
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
 - IWMPCore3.newMedia
---

# IWMPCore3::newMedia


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>newMedia</b> method retrieves a pointer to an <b>IWMPMedia</b> interface for a new media item.

## -parameters

### -param bstrURL [in]

<b>BSTR</b> containing the URL.

### -param ppMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface.

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

The <i>bstrURL</i> parameter must not be an empty string or null.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>