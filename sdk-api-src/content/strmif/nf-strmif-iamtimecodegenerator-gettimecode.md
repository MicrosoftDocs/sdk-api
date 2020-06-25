---
UID: NF:strmif.IAMTimecodeGenerator.GetTimecode
title: IAMTimecodeGenerator::GetTimecode (strmif.h)
description: The GetTimecode method retrieves the most recent timecode and/or userbit value available in the stream.
helpviewer_keywords: ["GetTimecode","GetTimecode method [DirectShow]","GetTimecode method [DirectShow]","IAMTimecodeGenerator interface","IAMTimecodeGenerator interface [DirectShow]","GetTimecode method","IAMTimecodeGenerator.GetTimecode","IAMTimecodeGenerator::GetTimecode","IAMTimecodeGeneratorGetTimecode","dshow.iamtimecodegenerator_gettimecode","strmif/IAMTimecodeGenerator::GetTimecode"]
old-location: dshow\iamtimecodegenerator_gettimecode.htm
tech.root: DirectShow
ms.assetid: 40f24a99-5a6b-4aff-b22c-e05811c910f4
ms.date: 12/05/2018
ms.keywords: GetTimecode, GetTimecode method [DirectShow], GetTimecode method [DirectShow],IAMTimecodeGenerator interface, IAMTimecodeGenerator interface [DirectShow],GetTimecode method, IAMTimecodeGenerator.GetTimecode, IAMTimecodeGenerator::GetTimecode, IAMTimecodeGeneratorGetTimecode, dshow.iamtimecodegenerator_gettimecode, strmif/IAMTimecodeGenerator::GetTimecode
f1_keywords:
- strmif/IAMTimecodeGenerator.GetTimecode
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
- IAMTimecodeGenerator.GetTimecode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeGenerator::GetTimecode


## -description



The <code>GetTimecode</code> method retrieves the most recent timecode and/or userbit value available in the stream.




## -parameters




### -param pTimecodeSample [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/aviriff/ns-aviriff-tagtimecode_sample">TIMECODE_SAMPLE</a> structure.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Use this method to obtain the most recent timecode value available in the stream. The application can use this to monitor the timecode and verify the generator is working properly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-settimecode">IAMTimecodeGenerator::SetTimecode</a>
 

 

