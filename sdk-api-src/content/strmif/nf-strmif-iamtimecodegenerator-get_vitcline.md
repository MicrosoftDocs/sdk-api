---
UID: NF:strmif.IAMTimecodeGenerator.get_VITCLine
title: IAMTimecodeGenerator::get_VITCLine (strmif.h)
description: The get_VITCLine method retrieves which line(s) the vertical interval timecode information has been inserted into.
helpviewer_keywords: ["IAMTimecodeGenerator interface [DirectShow]","get_VITCLine method","IAMTimecodeGenerator.get_VITCLine","IAMTimecodeGenerator::get_VITCLine","IAMTimecodeGeneratorget_VITCLine","dshow.iamtimecodegenerator_get_vitcline","get_VITCLine","get_VITCLine method [DirectShow]","get_VITCLine method [DirectShow]","IAMTimecodeGenerator interface","strmif/IAMTimecodeGenerator::get_VITCLine"]
old-location: dshow\iamtimecodegenerator_get_vitcline.htm
tech.root: dshow
ms.assetid: 0a1595a6-30ae-46ab-bfda-102b4dbc67ef
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],get_VITCLine method, IAMTimecodeGenerator.get_VITCLine, IAMTimecodeGenerator::get_VITCLine, IAMTimecodeGeneratorget_VITCLine, dshow.iamtimecodegenerator_get_vitcline, get_VITCLine, get_VITCLine method [DirectShow], get_VITCLine method [DirectShow],IAMTimecodeGenerator interface, strmif/IAMTimecodeGenerator::get_VITCLine
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
 - IAMTimecodeGenerator::get_VITCLine
 - strmif/IAMTimecodeGenerator::get_VITCLine
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
 - IAMTimecodeGenerator.get_VITCLine
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-put_vitcline">IAMTimecodeGenerator::put_VITCLine</a>