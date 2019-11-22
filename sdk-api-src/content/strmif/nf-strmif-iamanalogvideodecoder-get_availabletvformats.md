---
UID: NF:strmif.IAMAnalogVideoDecoder.get_AvailableTVFormats
title: IAMAnalogVideoDecoder::get_AvailableTVFormats (strmif.h)

description: The get_AvailableTVFormats method retrieves the analog video formats that the decoder supports.
old-location: dshow\iamanalogvideodecoder_get_availabletvformats.htm
tech.root: DirectShow
ms.assetid: 651f902f-de27-4185-b368-ce2cbf12cfae

ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_AvailableTVFormats method, IAMAnalogVideoDecoder.get_AvailableTVFormats, IAMAnalogVideoDecoder::get_AvailableTVFormats, IAMAnalogVideoDecoderget_AvailableTVFormats, dshow.iamanalogvideodecoder_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_AvailableTVFormats
ms.topic: method
f1_keywords: 
 - "strmif/IAMAnalogVideoDecoder.get_AvailableTVFormats"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAnalogVideoDecoder.get_AvailableTVFormats
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAnalogVideoDecoder::get_AvailableTVFormats


## -description



The <b>get_AvailableTVFormats</b> method retrieves the analog video formats that the decoder supports.




## -parameters




### -param lAnalogVideoStandard [out]

Pointer to a variable that receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>
 

 

