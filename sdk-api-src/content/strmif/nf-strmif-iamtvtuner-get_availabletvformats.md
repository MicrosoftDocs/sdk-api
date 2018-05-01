---
UID: NF:strmif.IAMTVTuner.get_AvailableTVFormats
title: IAMTVTuner::get_AvailableTVFormats method
author: windows-driver-content
description: The get_AvailableTVFormats method retrieves all the analog video TV standards that the tuner supports.
old-location: dshow\iamtvtuner_get_availabletvformats.htm
old-project: DirectShow
ms.assetid: 7b1a31d4-be05-4ab3-8ca3-b1a3f4bda03f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMTVTuner, IAMTVTuner interface [DirectShow], get_AvailableTVFormats method, IAMTVTuner::get_AvailableTVFormats, IAMTVTunerget_AvailableTVFormats, dshow.iamtvtuner_get_availabletvformats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow], IAMTVTuner interface, get_AvailableTVFormats,IAMTVTuner.get_AvailableTVFormats, strmif/IAMTVTuner::get_AvailableTVFormats
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTVTuner.get_AvailableTVFormats
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTVTuner::get_AvailableTVFormats method


## -description



The <code>get_AvailableTVFormats</code> method retrieves all the analog video TV standards that the tuner supports.




## -parameters




### -param lAnalogVideoStandard [out]

Pointer to a variable that receives a bitwise combination of values from the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

