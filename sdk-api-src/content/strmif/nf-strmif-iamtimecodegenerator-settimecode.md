---
UID: NF:strmif.IAMTimecodeGenerator.SetTimecode
title: IAMTimecodeGenerator::SetTimecode (strmif.h)
description: The SetTimecode method sets the timecode, userbit value, or both.
helpviewer_keywords: ["IAMTimecodeGenerator interface [DirectShow]","SetTimecode method","IAMTimecodeGenerator.SetTimecode","IAMTimecodeGenerator::SetTimecode","IAMTimecodeGeneratorSetTimecode","SetTimecode","SetTimecode method [DirectShow]","SetTimecode method [DirectShow]","IAMTimecodeGenerator interface","dshow.iamtimecodegenerator_settimecode","strmif/IAMTimecodeGenerator::SetTimecode"]
old-location: dshow\iamtimecodegenerator_settimecode.htm
tech.root: dshow
ms.assetid: 6da4b7e0-e6cd-4555-b5a3-e5f0f20ff070
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],SetTimecode method, IAMTimecodeGenerator.SetTimecode, IAMTimecodeGenerator::SetTimecode, IAMTimecodeGeneratorSetTimecode, SetTimecode, SetTimecode method [DirectShow], SetTimecode method [DirectShow],IAMTimecodeGenerator interface, dshow.iamtimecodegenerator_settimecode, strmif/IAMTimecodeGenerator::SetTimecode
f1_keywords:
- strmif/IAMTimecodeGenerator.SetTimecode
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
- IAMTimecodeGenerator.SetTimecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeGenerator::SetTimecode


## -description



The <code>SetTimecode</code> method sets the timecode, userbit value, or both.




## -parameters




### -param pTimecodeSample [in]

Pointer to a <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



To set only timecode, set userbit value to <b>NULL</b>, and vice versa. If generator is running, these values will take effect immediately.




## -see-also


<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-gettimecode">IAMTimecodeGenerator::GetTimecode</a>

