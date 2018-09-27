---
UID: NF:strmif.IAMTimecodeGenerator.SetTCGMode
title: IAMTimecodeGenerator::SetTCGMode
author: windows-sdk-content
description: The SetTCGMode method sets the SMPTE timecode generator properties.
old-location: dshow\iamtimecodegenerator_settcgmode.htm
tech.root: DirectShow
ms.assetid: 61434534-0a43-4bf3-81d1-3b27ac601cb4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAMTimecodeGenerator interface [DirectShow],SetTCGMode method, IAMTimecodeGenerator.SetTCGMode, IAMTimecodeGenerator::SetTCGMode, IAMTimecodeGeneratorSetTCGMode, SetTCGMode, SetTCGMode method [DirectShow], SetTCGMode method [DirectShow],IAMTimecodeGenerator interface, dshow.iamtimecodegenerator_settcgmode, strmif/IAMTimecodeGenerator::SetTCGMode
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
 - IAMTimecodeGenerator.SetTCGMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



For more information on ED_TCG_TIMECODE_TYPE, see the <a href="https://msdn.microsoft.com/dd9f5310-b1c0-46ff-b038-d6a50ac400a2">IAMTimecodeReader::SetTCRMode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>



<a href="https://msdn.microsoft.com/76a754e3-4071-437a-bd98-99a94e2594a3">IAMTimecodeGenerator::GetTCGMode</a>
 

 

