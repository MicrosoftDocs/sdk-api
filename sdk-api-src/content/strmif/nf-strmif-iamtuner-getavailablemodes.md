---
UID: NF:strmif.IAMTuner.GetAvailableModes
title: IAMTuner::GetAvailableModes (strmif.h)
description: The GetAvailableModes method retrieves the tuner's supported modes.
old-location: dshow\iamtuner_getavailablemodes.htm
tech.root: DirectShow
ms.assetid: 74025309-2aab-4e0f-95bc-8e6a1e2a5bb4
ms.date: 12/05/2018
ms.keywords: GetAvailableModes, GetAvailableModes method [DirectShow], GetAvailableModes method [DirectShow],IAMTuner interface, IAMTuner interface [DirectShow],GetAvailableModes method, IAMTuner.GetAvailableModes, IAMTuner::GetAvailableModes, IAMTunerGetAvailableModes, dshow.iamtuner_getavailablemodes, strmif/IAMTuner::GetAvailableModes
f1_keywords:
- strmif/IAMTuner.GetAvailableModes
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
- IAMTuner.GetAvailableModes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTuner::GetAvailableModes


## -description



The <code>GetAvailableModes</code> method retrieves the tuner's supported modes.




## -parameters




### -param plModes [out]

Pointer to a variable that receives any combination of the values as specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-amtunermodetype">AMTunerModeType</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

