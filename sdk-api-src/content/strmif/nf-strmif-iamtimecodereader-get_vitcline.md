---
UID: NF:strmif.IAMTimecodeReader.get_VITCLine
title: IAMTimecodeReader::get_VITCLine (strmif.h)
author: windows-sdk-content
description: The get_VITCLine method retrieves the vertical interval line that the timecode reader is using to read timecode.
old-location: dshow\iamtimecodereader_get_vitcline.htm
tech.root: DirectShow
ms.assetid: 04eda79a-1301-4bc1-855e-1cb0c4451797
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTimecodeReader interface [DirectShow],get_VITCLine method, IAMTimecodeReader.get_VITCLine, IAMTimecodeReader::get_VITCLine, IAMTimecodeReaderget_VITCLine, dshow.iamtimecodereader_get_vitcline, get_VITCLine, get_VITCLine method [DirectShow], get_VITCLine method [DirectShow],IAMTimecodeReader interface, strmif/IAMTimecodeReader::get_VITCLine
ms.topic: method
f1_keywords: 
 - "strmif/IAMTimecodeReader.get_VITCLine"
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
 - IAMTimecodeReader.get_VITCLine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeReader::get_VITCLine


## -description



The <code>get_VITCLine</code> method retrieves the vertical interval line that the timecode reader is using to read timecode.



This method is not implemented.


## -parameters




### -param pLine [out]

Pointer to the vertical line containing timecode information (valid lines are from 11 through 20).


## -returns



Returns E_NOTIMPL.




## -remarks



The high bit indicates that multiple lines are used and successive calls will cycle through the line numbers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-put_vitcline">IAMTimecodeReader::put_VITCLine</a>
 

 

