---
UID: NF:strmif.IAMTVTuner.StoreAutoTune
title: IAMTVTuner::StoreAutoTune (strmif.h)
author: windows-sdk-content
description: The StoreAutoTune method saves the fine-tuning information for all channels.
old-location: dshow\iamtvtuner_storeautotune.htm
tech.root: DirectShow
ms.assetid: 6e39d757-d8bd-4011-9a67-6bf57b5d820b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],StoreAutoTune method, IAMTVTuner.StoreAutoTune, IAMTVTuner::StoreAutoTune, IAMTVTunerStoreAutoTune, StoreAutoTune, StoreAutoTune method [DirectShow], StoreAutoTune method [DirectShow],IAMTVTuner interface, dshow.iamtvtuner_storeautotune, strmif/IAMTVTuner::StoreAutoTune
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
 - IAMTVTuner.StoreAutoTune
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVTuner::StoreAutoTune


## -description



The <code>StoreAutoTune</code> method saves the fine-tuning information for all channels.




## -parameters






## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Override the channel-to-frequency information stored by this method by setting a new country/region code in the <a href="https://msdn.microsoft.com/d733f829-5600-4f75-9bc9-de8dc8dd8031">IAMTuner::put_CountryCode</a> method. For a listing of country/region codes, see <a href="https://msdn.microsoft.com/9a0e8c77-05f6-496a-bd7c-8c73953fe7c2">International Analog TV Tuning</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

