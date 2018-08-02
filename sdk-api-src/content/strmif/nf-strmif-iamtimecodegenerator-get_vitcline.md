---
UID: NF:strmif.IAMTimecodeGenerator.get_VITCLine
title: IAMTimecodeGenerator::get_VITCLine
author: windows-sdk-content
description: The get_VITCLine method retrieves which line(s) the vertical interval timecode information has been inserted into.
old-location: dshow\iamtimecodegenerator_get_vitcline.htm
old-project: DirectShow
ms.assetid: 0a1595a6-30ae-46ab-bfda-102b4dbc67ef
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],get_VITCLine method, IAMTimecodeGenerator.get_VITCLine, IAMTimecodeGenerator::get_VITCLine, IAMTimecodeGeneratorget_VITCLine, dshow.iamtimecodegenerator_get_vitcline, get_VITCLine, get_VITCLine method [DirectShow], get_VITCLine method [DirectShow],IAMTimecodeGenerator interface, strmif/IAMTimecodeGenerator::get_VITCLine
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
 - IAMTimecodeGenerator.get_VITCLine
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeGenerator::get_VITCLine


## -description



The <code>get_VITCLine</code> method retrieves which line(s) the vertical interval timecode information has been inserted into.




## -parameters




### -param pLine [out]

Pointer to the vertical line(s) containing the timecode information (valid lines are 11-20).


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



To get VITC information from multiple lines, make successive calls to this method, once for each line desired, with the hi bit set for each line.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>



<a href="https://msdn.microsoft.com/351bf80b-f14c-454f-9d20-ceff4a437fcd">IAMTimecodeGenerator::put_VITCLine</a>
 

 

