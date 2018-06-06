---
UID: NF:strmif.IAMTimecodeGenerator.GetTimecode
title: IAMTimecodeGenerator::GetTimecode
author: windows-sdk-content
description: The GetTimecode method retrieves the most recent timecode and/or userbit value available in the stream.
old-location: dshow\iamtimecodegenerator_gettimecode.htm
old-project: DirectShow
ms.assetid: 40f24a99-5a6b-4aff-b22c-e05811c910f4
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetTimecode, GetTimecode method [DirectShow], GetTimecode method [DirectShow],IAMTimecodeGenerator interface, IAMTimecodeGenerator interface [DirectShow],GetTimecode method, IAMTimecodeGenerator.GetTimecode, IAMTimecodeGenerator::GetTimecode, IAMTimecodeGeneratorGetTimecode, dshow.iamtimecodegenerator_gettimecode, strmif/IAMTimecodeGenerator::GetTimecode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeGenerator::GetTimecode


## -description



The <code>GetTimecode</code> method retrieves the most recent timecode and/or userbit value available in the stream.




## -parameters




### -param pTimecodeSample [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568528">TIMECODE_SAMPLE</a> structure.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Use this method to obtain the most recent timecode value available in the stream. The application can use this to monitor the timecode and verify the generator is working properly.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>



<a href="https://msdn.microsoft.com/6da4b7e0-e6cd-4555-b5a3-e5f0f20ff070">IAMTimecodeGenerator::SetTimecode</a>
 

 

