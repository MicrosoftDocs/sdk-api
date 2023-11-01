---
UID: NF:wmpservices.IWMPServices.GetStreamTime
title: IWMPServices::GetStreamTime (wmpservices.h)
description: The IWMPServices::GetStreamTime method retrieves a structure indicating the current stream time.
helpviewer_keywords: ["GetStreamTime","GetStreamTime method [Windows Media Player]","GetStreamTime method [Windows Media Player]","IWMPServices interface","IWMPServices interface [Windows Media Player]","GetStreamTime method","IWMPServices.GetStreamTime","IWMPServices::GetStreamTime","IWMPServicesGetStreamTimeDSP","wmp.iwmpservices_getstreamtime","wmpservices/IWMPServices::GetStreamTime"]
old-location: wmp\iwmpservices_getstreamtime.htm
tech.root: WMP
ms.assetid: 4e6c8181-3ff9-4ce1-aad5-9d7821771f69
ms.date: 4/26/2023
ms.keywords: GetStreamTime, GetStreamTime method [Windows Media Player], GetStreamTime method [Windows Media Player],IWMPServices interface, IWMPServices interface [Windows Media Player],GetStreamTime method, IWMPServices.GetStreamTime, IWMPServices::GetStreamTime, IWMPServicesGetStreamTimeDSP, wmp.iwmpservices_getstreamtime, wmpservices/IWMPServices::GetStreamTime
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
 - IWMPServices::GetStreamTime
 - wmpservices/IWMPServices::GetStreamTime
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
 - IWMPServices.GetStreamTime
---

# IWMPServices::GetStreamTime


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPServices::GetStreamTime</b> method retrieves a structure indicating the current stream time.

## -parameters

### -param prt [in]

Pointer to a <b>REFERENCE_TIME</b> structure.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

The current stream time is determined by Windows Media Player. This means that the value returned by this method do not necessarily represent the elapsed time relative to the beginning of the file. For instance, if the user moves the trackbar in the Player to seek the media to a new position, the value returned by this method returns the time elapsed since the media began playing from the new position. Changes in playback rate will also affect the value returned by this method.

The values provided in the <b>rtTimestamp</b> member of <b>IMediaObject::ProcessInput</b> and the <b>rtTimestamp</b> member of the <b>DMO_OUTPUT_DATA_BUFFER</b> structure supplied by <b>IMediaObject::ProcessOutput</b> contain values that indicate when the data provided in the buffer will be rendered relative to the current stream time. Therefore, these values also do not necessarily represent the elapsed time relative to the beginning of the file or the presentation time specified in the file.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices">IWMPServices Interface</a>