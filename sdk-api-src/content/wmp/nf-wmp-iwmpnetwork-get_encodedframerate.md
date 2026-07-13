---
UID: NF:wmp.IWMPNetwork.get_encodedFrameRate
title: IWMPNetwork::get_encodedFrameRate (wmp.h)
description: The get_encodedFrameRate method retrieves the video frame rate specified by the content author.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_encodedFrameRate method","IWMPNetwork.get_encodedFrameRate","IWMPNetwork::get_encodedFrameRate","IWMPNetworkget_encodedFrameRate","get_encodedFrameRate","get_encodedFrameRate method [Windows Media Player]","get_encodedFrameRate method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_encodedframerate","wmp/IWMPNetwork::get_encodedFrameRate"]
old-location: wmp\iwmpnetwork_get_encodedframerate.htm
tech.root: WMP
ms.assetid: d42133cf-3b81-4d22-b83d-d8a5756d9d9c
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_encodedFrameRate method, IWMPNetwork.get_encodedFrameRate, IWMPNetwork::get_encodedFrameRate, IWMPNetworkget_encodedFrameRate, get_encodedFrameRate, get_encodedFrameRate method [Windows Media Player], get_encodedFrameRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_encodedframerate, wmp/IWMPNetwork::get_encodedFrameRate
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
 - IWMPNetwork::get_encodedFrameRate
 - wmp/IWMPNetwork::get_encodedFrameRate
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
 - IWMPNetwork.get_encodedFrameRate
---

# IWMPNetwork::get_encodedFrameRate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_encodedFrameRate</b> method retrieves the video frame rate specified by the content author.

## -parameters

### -param plFrameRate [out]

Pointer to a <b>long</b> containing the frame rate in frames per second (fps).

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

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_framerate">IWMPNetwork::get_frameRate</a>