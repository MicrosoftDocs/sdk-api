---
UID: NF:wmp.IWMPCore.get_mediaCollection
title: IWMPCore::get_mediaCollection (wmp.h)
description: The get_mediaCollection method retrieves a pointer to an IWMPMediaCollection interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_mediaCollection method","IWMPCore.get_mediaCollection","IWMPCore::get_mediaCollection","IWMPCoreget_mediaCollection","get_mediaCollection","get_mediaCollection method [Windows Media Player]","get_mediaCollection method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_mediacollection","wmp/IWMPCore::get_mediaCollection"]
old-location: wmp\iwmpcore_get_mediacollection.htm
tech.root: WMP
ms.assetid: 41b090ca-edf0-440e-b578-26c5ad064657
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_mediaCollection method, IWMPCore.get_mediaCollection, IWMPCore::get_mediaCollection, IWMPCoreget_mediaCollection, get_mediaCollection, get_mediaCollection method [Windows Media Player], get_mediaCollection method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_mediacollection, wmp/IWMPCore::get_mediaCollection
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
 - IWMPCore::get_mediaCollection
 - wmp/IWMPCore::get_mediaCollection
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
 - IWMPCore.get_mediaCollection
---

# IWMPCore::get_mediaCollection


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_mediaCollection</b> method retrieves a pointer to an <b>IWMPMediaCollection</b> interface.

## -parameters

### -param ppMediaCollection [out]

Pointer to a pointer to an <b>IWMPMediaCollection</b> interface.

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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>