---
UID: NF:strmif.IAMTimecodeGenerator.SetTCGMode
title: IAMTimecodeGenerator::SetTCGMode (strmif.h)
description: The SetTCGMode method sets the SMPTE timecode generator properties.
helpviewer_keywords: ["IAMTimecodeGenerator interface [DirectShow]","SetTCGMode method","IAMTimecodeGenerator.SetTCGMode","IAMTimecodeGenerator::SetTCGMode","IAMTimecodeGeneratorSetTCGMode","SetTCGMode","SetTCGMode method [DirectShow]","SetTCGMode method [DirectShow]","IAMTimecodeGenerator interface","dshow.iamtimecodegenerator_settcgmode","strmif/IAMTimecodeGenerator::SetTCGMode"]
old-location: dshow\iamtimecodegenerator_settcgmode.htm
tech.root: dshow
ms.assetid: 61434534-0a43-4bf3-81d1-3b27ac601cb4
ms.date: 12/05/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],SetTCGMode method, IAMTimecodeGenerator.SetTCGMode, IAMTimecodeGenerator::SetTCGMode, IAMTimecodeGeneratorSetTCGMode, SetTCGMode, SetTCGMode method [DirectShow], SetTCGMode method [DirectShow],IAMTimecodeGenerator interface, dshow.iamtimecodegenerator_settcgmode, strmif/IAMTimecodeGenerator::SetTCGMode
f1_keywords:
- strmif/IAMTimecodeGenerator.SetTCGMode
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
- IAMTimecodeGenerator.SetTCGMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTimecodeGenerator::SetTCGMode


## -description



The <code>SetTCGMode</code> method sets the SMPTE timecode generator properties.




## -parameters




### -param Param [in]

Timecode generator mode. Specify one of the following modes.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG_FRAMERATE</td>
<td>Frame rate</td>
</tr>
<tr>
<td>ED_TCG_REFERENCE_SOURCE</td>
<td>Source of the count value</td>
</tr>
<tr>
<td>ED_TCG_SYNC_SOURCE</td>
<td>Source of the hardware clock reference</td>
</tr>
<tr>
<td>ED_TCG_TIMECODE_TYPE</td>
<td>SMPTE timecode format of the generator</td>
</tr>
</table>
 


### -param Value [in]

Setting of the mode specified in <i>Param</i>.

If ED_TCG_FRAMERATE is specified in <i>Param</i>, this parameter is set to one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_FORMAT_SMPTE_24</td>
<td>24 frames per second.</td>
</tr>
<tr>
<td>ED_FORMAT_SMPTE_25</td>
<td>25 frames per second.</td>
</tr>
<tr>
<td>ED_FORMAT_SMPTE_30</td>
<td>30 frames per second. Nondrop frame.</td>
</tr>
<tr>
<td>ED_FORMAT_SMPTE_30DROP</td>
<td>30 frames per second. Drop frame (actually 29.97 frames per second).</td>
</tr>
</table>
 

If ED_TCG_REFERENCE_SOURCE is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG_FREE</td>
<td>No count reference source.</td>
</tr>
<tr>
<td>ED_TCG_READER</td>
<td>Sync to reader value (jamsync).</td>
</tr>
</table>
 

If ED_TCG_SYNC_SOURCE is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG_FREE</td>
<td>Lock to nothing (freerun).</td>
</tr>
<tr>
<td>ED_TCG_READER</td>
<td>Lock to timecode reader.</td>
</tr>
<tr>
<td>ED_TCG_VIDEO</td>
<td>Lock to incoming video.</td>
</tr>
</table>
 

If ED_TCG_TIMECODE_TYPE is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG_MIDI_FULL</td>
<td>MIDI Full Frame timecode</td>
</tr>
<tr>
<td>ED_TCG_MIDI_QF</td>
<td>MIDI quarter frame timecode</td>
</tr>
<tr>
<td>ED_TCG_SMPTE_LTC</td>
<td>Linear timecode</td>
</tr>
<tr>
<td>ED_TCG_SMPTE_VITC</td>
<td>Vertical interval timecode</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



For more information on ED_TCG_TIMECODE_TYPE, see the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-settcrmode">IAMTimecodeReader::SetTCRMode</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-gettcgmode">IAMTimecodeGenerator::GetTCGMode</a>
 

 

