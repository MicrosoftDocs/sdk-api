---
UID: NF:wmp.IWMPNetwork.get_framesSkipped
title: IWMPNetwork::get_framesSkipped (wmp.h)
description: The get_framesSkipped method retrieves the total number of frames skipped during playback.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_framesSkipped method","IWMPNetwork.get_framesSkipped","IWMPNetwork::get_framesSkipped","IWMPNetworkget_framesSkipped","get_framesSkipped","get_framesSkipped method [Windows Media Player]","get_framesSkipped method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_framesskipped","wmp/IWMPNetwork::get_framesSkipped"]
old-location: wmp\iwmpnetwork_get_framesskipped.htm
tech.root: WMP
ms.assetid: 2ca3e280-4f3e-4460-884d-186199e3edd6
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_framesSkipped method, IWMPNetwork.get_framesSkipped, IWMPNetwork::get_framesSkipped, IWMPNetworkget_framesSkipped, get_framesSkipped, get_framesSkipped method [Windows Media Player], get_framesSkipped method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_framesskipped, wmp/IWMPNetwork::get_framesSkipped
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
 - IWMPNetwork::get_framesSkipped
 - wmp/IWMPNetwork::get_framesSkipped
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
 - IWMPNetwork.get_framesSkipped
---

# IWMPNetwork::get_framesSkipped


## -description

The <b>get_framesSkipped</b> method retrieves the total number of frames skipped during playback.

## -parameters

### -param plFrames [out]

Pointer to a <b>long</b> containing the number of frames.

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