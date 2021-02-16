---
UID: NF:strmif.IAMTimecodeReader.put_VITCLine
title: IAMTimecodeReader::put_VITCLine (strmif.h)
description: The put_VITCLine method specifies the vertical interval line that the timecode reader will use to read timecode.
helpviewer_keywords: ["IAMTimecodeReader interface [DirectShow]","put_VITCLine method","IAMTimecodeReader.put_VITCLine","IAMTimecodeReader::put_VITCLine","IAMTimecodeReaderput_VITCLine","dshow.iamtimecodereader_put_vitcline","put_VITCLine","put_VITCLine method [DirectShow]","put_VITCLine method [DirectShow]","IAMTimecodeReader interface","strmif/IAMTimecodeReader::put_VITCLine"]
old-location: dshow\iamtimecodereader_put_vitcline.htm
tech.root: dshow
ms.assetid: 171b0fd2-1498-41ae-9803-99b9128ee305
ms.date: 12/05/2018
ms.keywords: IAMTimecodeReader interface [DirectShow],put_VITCLine method, IAMTimecodeReader.put_VITCLine, IAMTimecodeReader::put_VITCLine, IAMTimecodeReaderput_VITCLine, dshow.iamtimecodereader_put_vitcline, put_VITCLine, put_VITCLine method [DirectShow], put_VITCLine method [DirectShow],IAMTimecodeReader interface, strmif/IAMTimecodeReader::put_VITCLine
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTimecodeReader::put_VITCLine
 - strmif/IAMTimecodeReader::put_VITCLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeReader.put_VITCLine
---

# IAMTimecodeReader::put_VITCLine


## -description

The <code>put_VITCLine</code> method specifies the vertical interval line that the timecode reader will use to read timecode.



This method is not implemented.

## -parameters

### -param Line [in]

Vertical line containing timecode information (valid lines are 11-20; 0 means autoselect).

## -returns

Returns E_NOTIMPL.

## -remarks

If VITC mode is specified in the <a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-settcrmode">IAMTimecodeReader::SetTCRMode</a> method, you must specify which line or lines will contain timecode information. To read VITC on specific multiple lines, the caller would make successive calls to <code>IAMTimecodeReader::put_VITCLine</code>, once for each line desired.

Set the high bit to add to the list of lines for readers that test across multiple lines.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-get_vitcline">IAMTimecodeReader::get_VITCLine</a>