---
UID: NF:strmif.IAMTimecodeGenerator.SetTimecode
title: IAMTimecodeGenerator::SetTimecode
author: windows-sdk-content
description: The SetTimecode method sets the timecode, userbit value, or both.
old-location: dshow\iamtimecodegenerator_settimecode.htm
tech.root: DirectShow
ms.assetid: 6da4b7e0-e6cd-4555-b5a3-e5f0f20ff070
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],SetTimecode method, IAMTimecodeGenerator.SetTimecode, IAMTimecodeGenerator::SetTimecode, IAMTimecodeGeneratorSetTimecode, SetTimecode, SetTimecode method [DirectShow], SetTimecode method [DirectShow],IAMTimecodeGenerator interface, dshow.iamtimecodegenerator_settimecode, strmif/IAMTimecodeGenerator::SetTimecode
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
 - IAMTimecodeGenerator.SetTimecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTimecodeGenerator::SetTimecode


## -description



The <code>SetTimecode</code> method sets the timecode, userbit value, or both.




## -parameters




### -param pTimecodeSample [in]

Pointer to a <a href="https://msdn.microsoft.com/7b17e152-99eb-4d6d-a8b1-bf4ef7ab83be">TIMECODE_SAMPLE</a> structure.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



To set only timecode, set userbit value to <b>NULL</b>, and vice versa. If generator is running, these values will take effect immediately.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>



<a href="https://msdn.microsoft.com/40f24a99-5a6b-4aff-b22c-e05811c910f4">IAMTimecodeGenerator::GetTimecode</a>
 

 

