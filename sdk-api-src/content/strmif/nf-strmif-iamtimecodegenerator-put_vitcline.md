---
UID: NF:strmif.IAMTimecodeGenerator.put_VITCLine
title: IAMTimecodeGenerator::put_VITCLine
author: windows-sdk-content
description: The put_VITCLine method specifies which line to insert the vertical interval timecode information into.
old-location: dshow\iamtimecodegenerator_put_vitcline.htm
old-project: DirectShow
ms.assetid: 351bf80b-f14c-454f-9d20-ceff4a437fcd
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],put_VITCLine method, IAMTimecodeGenerator.put_VITCLine, IAMTimecodeGenerator::put_VITCLine, IAMTimecodeGeneratorput_VITCLine, dshow.iamtimecodegenerator_put_vitcline, put_VITCLine, put_VITCLine method [DirectShow], put_VITCLine method [DirectShow],IAMTimecodeGenerator interface, strmif/IAMTimecodeGenerator::put_VITCLine
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
 - IAMTimecodeGenerator.put_VITCLine
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeGenerator::put_VITCLine


## -description



The <code>put_VITCLine</code> method specifies which line to insert the vertical interval timecode information into.




## -parameters




### -param Line [in]

Vertical line to contain the timecode information (valid lines are 11-20; 0 means autoselect).


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



To generate VITC on specific multiple lines, make successive calls to this method, once for each line desired.

Set the high bit to add to this line to any previously set lines.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>



<a href="https://msdn.microsoft.com/0a1595a6-30ae-46ab-bfda-102b4dbc67ef">IAMTimecodeGenerator::get_VITCLine</a>
 

 

