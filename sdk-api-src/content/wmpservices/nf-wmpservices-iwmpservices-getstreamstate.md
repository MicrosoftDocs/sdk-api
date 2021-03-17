---
UID: NF:wmpservices.IWMPServices.GetStreamState
title: IWMPServices::GetStreamState (wmpservices.h)
description: The IWMPServices::GetStreamState method retrieves information about the current play state of the stream.
helpviewer_keywords: ["GetStreamState","GetStreamState method [Windows Media Player]","GetStreamState method [Windows Media Player]","IWMPServices interface","IWMPServices interface [Windows Media Player]","GetStreamState method","IWMPServices.GetStreamState","IWMPServices::GetStreamState","IWMPServicesGetStreamStateDSP","wmp.iwmpservices_getstreamstate","wmpservices/IWMPServices::GetStreamState"]
old-location: wmp\iwmpservices_getstreamstate.htm
tech.root: WMP
ms.assetid: 1a73ea54-45ce-47ff-b551-10aab2798420
ms.date: 12/05/2018
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