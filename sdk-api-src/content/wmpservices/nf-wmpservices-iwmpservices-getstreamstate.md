---
UID: NF:wmpservices.IWMPServices.GetStreamState
title: IWMPServices::GetStreamState (wmpservices.h)
description: The IWMPServices::GetStreamState method retrieves information about the current play state of the stream.
helpviewer_keywords: ["GetStreamState","GetStreamState method [Windows Media Player]","GetStreamState method [Windows Media Player]","IWMPServices interface","IWMPServices interface [Windows Media Player]","GetStreamState method","IWMPServices.GetStreamState","IWMPServices::GetStreamState","IWMPServicesGetStreamStateDSP","wmp.iwmpservices_getstreamstate","wmpservices/IWMPServices::GetStreamState"]
old-location: wmp\iwmpservices_getstreamstate.htm
tech.root: WMP
ms.assetid: 1a73ea54-45ce-47ff-b551-10aab2798420
ms.date: 4/26/2023
ms.keywords: GetStreamState, GetStreamState method [Windows Media Player], GetStreamState method [Windows Media Player],IWMPServices interface, IWMPServices interface [Windows Media Player],GetStreamState method, IWMPServices.GetStreamState, IWMPServices::GetStreamState, IWMPServicesGetStreamStateDSP, wmp.iwmpservices_getstreamstate, wmpservices/IWMPServices::GetStreamState
req.header: wmpservices.h
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
 - IWMPServices::GetStreamState
 - wmpservices/IWMPServices::GetStreamState
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
 - IWMPServices.GetStreamState
---

# IWMPServices::GetStreamState


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPServices::GetStreamState</b> method retrieves information about the current play state of the stream.

## -parameters

### -param pState [in]

A pointer to a <b>WMPServices_StreamState</b> enumeration value.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

The stream is stopped, paused, or playing.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices">IWMPServices Interface</a>



<a href="/windows/desktop/api/wmpservices/ne-wmpservices-wmpservices_streamstate">WMPServices_StreamState</a>