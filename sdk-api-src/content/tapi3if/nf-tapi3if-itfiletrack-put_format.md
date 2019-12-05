---
UID: NF:tapi3if.ITFileTrack.put_Format
title: ITFileTrack::put_Format (tapi3if.h)
description: The put_Format method sets the format type of the track.
old-location: tapi3\itfiletrack_put_format.htm
tech.root: Tapi
ms.assetid: 76a60e3f-d310-457d-8d1b-17860165c1e9
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],put_Format method, ITFileTrack.put_Format, ITFileTrack::put_Format, _tapi3_itfiletrack_put_format, put_Format, put_Format method [TAPI 2.2], put_Format method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_put_format, tapi3if/ITFileTrack::put_Format
ms.topic: method
f1_keywords:
- tapi3if/ITFileTrack.put_Format
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITFileTrack.put_Format
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITFileTrack::put_Format


## -description


The 
<b>put_Format</b> method sets the format type of the track.


## -parameters




### -param pmt [in]

 The
<b>AM_MEDIA_TYPE</b> descriptor of the file track format. For more information about <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. The <a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a> only supports the <b>FORMAT_WaveFormatEx</b> format type  in the <b>AM_MEDIA_TYPE</b> structure.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack">ITFileTrack</a>
 

 

