---
UID: NF:wmp.IWMPNetwork.get_frameRate
title: IWMPNetwork::get_frameRate (wmp.h)
description: The get_frameRate method retrieves the current video frame rate.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_frameRate method","IWMPNetwork.get_frameRate","IWMPNetwork::get_frameRate","IWMPNetworkget_frameRate","get_frameRate","get_frameRate method [Windows Media Player]","get_frameRate method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_framerate","wmp/IWMPNetwork::get_frameRate"]
old-location: wmp\iwmpnetwork_get_framerate.htm
tech.root: WMP
ms.assetid: 1521c462-b054-46d6-8646-4d20a836eadc
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],get_frameRate method, IWMPNetwork.get_frameRate, IWMPNetwork::get_frameRate, IWMPNetworkget_frameRate, get_frameRate, get_frameRate method [Windows Media Player], get_frameRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_framerate, wmp/IWMPNetwork::get_frameRate
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
 - IWMPNetwork::get_frameRate
 - wmp/IWMPNetwork::get_frameRate
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
 - IWMPNetwork.get_frameRate
---

# IWMPNetwork::get_frameRate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_frameRate</b> method retrieves the current video frame rate.

## -parameters

### -param plFrameRate [out]

Pointer to a <b>long</b> containing the frame rate.

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

The frame rate value is returned in frames per hundred seconds. For example, a value of 2998 indicates 29.98 frames per second (fps).

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_encodedframerate">IWMPNetwork::get_encodedFrameRate</a>