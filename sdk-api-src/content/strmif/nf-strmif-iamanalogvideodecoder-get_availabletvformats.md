---
UID: NF:strmif.IAMAnalogVideoDecoder.get_AvailableTVFormats
title: IAMAnalogVideoDecoder::get_AvailableTVFormats
author: windows-sdk-content
description: The get_AvailableTVFormats method retrieves the analog video formats that the decoder supports.
old-location: dshow\iamanalogvideodecoder_get_availabletvformats.htm
tech.root: DirectShow
ms.assetid: 651f902f-de27-4185-b368-ce2cbf12cfae
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_AvailableTVFormats method, IAMAnalogVideoDecoder.get_AvailableTVFormats, IAMAnalogVideoDecoder::get_AvailableTVFormats, IAMAnalogVideoDecoderget_AvailableTVFormats, dshow.iamanalogvideodecoder_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_AvailableTVFormats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMAnalogVideoDecoder.get_AvailableTVFormats
: 
---

# IAMAnalogVideoDecoder::get_AvailableTVFormats


## -description



The <b>get_AvailableTVFormats</b> method retrieves the analog video formats that the decoder supports.




## -parameters




### -param lAnalogVideoStandard [out]

Pointer to a variable that receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/81d43941-7c81-4220-915f-0b373a7455e5">IAMAnalogVideoDecoder Interface</a>
 

 

