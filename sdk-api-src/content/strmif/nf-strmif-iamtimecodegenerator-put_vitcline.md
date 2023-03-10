---
UID: NF:strmif.IAMTimecodeGenerator.put_VITCLine
title: IAMTimecodeGenerator::put_VITCLine (strmif.h)
description: The put_VITCLine method specifies which line to insert the vertical interval timecode information into.
helpviewer_keywords: ["IAMTimecodeGenerator interface [DirectShow]","put_VITCLine method","IAMTimecodeGenerator.put_VITCLine","IAMTimecodeGenerator::put_VITCLine","IAMTimecodeGeneratorput_VITCLine","dshow.iamtimecodegenerator_put_vitcline","put_VITCLine","put_VITCLine method [DirectShow]","put_VITCLine method [DirectShow]","IAMTimecodeGenerator interface","strmif/IAMTimecodeGenerator::put_VITCLine"]
old-location: dshow\iamtimecodegenerator_put_vitcline.htm
tech.root: dshow
ms.assetid: 351bf80b-f14c-454f-9d20-ceff4a437fcd
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],put_VITCLine method, IAMTimecodeGenerator.put_VITCLine, IAMTimecodeGenerator::put_VITCLine, IAMTimecodeGeneratorput_VITCLine, dshow.iamtimecodegenerator_put_vitcline, put_VITCLine, put_VITCLine method [DirectShow], put_VITCLine method [DirectShow],IAMTimecodeGenerator interface, strmif/IAMTimecodeGenerator::put_VITCLine
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
 - IAMTimecodeGenerator::put_VITCLine
 - strmif/IAMTimecodeGenerator::put_VITCLine
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
 - IAMTimecodeGenerator.put_VITCLine
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-get_vitcline">IAMTimecodeGenerator::get_VITCLine</a>