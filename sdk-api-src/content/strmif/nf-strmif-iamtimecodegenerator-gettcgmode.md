---
UID: NF:strmif.IAMTimecodeGenerator.GetTCGMode
title: IAMTimecodeGenerator::GetTCGMode
author: windows-sdk-content
description: The GetTCGMode method retrieves the SMPTE timecode generator properties.
old-location: dshow\iamtimecodegenerator_gettcgmode.htm
old-project: DirectShow
ms.assetid: 76a754e3-4071-437a-bd98-99a94e2594a3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTCGMode, GetTCGMode method [DirectShow], GetTCGMode method [DirectShow],IAMTimecodeGenerator interface, IAMTimecodeGenerator interface [DirectShow],GetTCGMode method, IAMTimecodeGenerator.GetTCGMode, IAMTimecodeGenerator::GetTCGMode, IAMTimecodeGeneratorGetTCGMode, dshow.iamtimecodegenerator_gettcgmode, strmif/IAMTimecodeGenerator::GetTCGMode
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
 - IAMTimecodeGenerator.GetTCGMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeGenerator::GetTCGMode


## -description



The <code>GetTCGMode</code> method retrieves the SMPTE timecode generator properties.




## -parameters




### -param Param [in]

Timecode generator mode. Specify one of the following modes you want to get settings for.

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
 


### -param pValue [out]

Pointer to the current setting of the mode specified in <i>Param</i>.

If you specify ED_TCG_FRAMERATE in <i>Param</i>, this parameter retrieves one of the following.

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
<td>30 frames per second. Drop frame (actually 29.97 fps).</td>
</tr>
</table>
 

If you specify ED_TCG_REFERENCE_SOURCE in <i>Param</i>, this parameter retrieves one of the following.

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
<td>Synchronize to reader value (jamsync).</td>
</tr>
</table>
 

If you specify ED_TCG_SYNC_SOURCE in <i>Param</i>, this parameter retrieves one of the following.

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
 

If you specify ED_TCG_TIMECODE_TYPE in <i>Param</i>, this parameter retrieves one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG_MIDI_FULL</td>
<td>MIDI full frame timecode</td>
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



This method returns various settings of the timecode generator. For more information on ED_TCG_TIMECODE_TYPE, see <a href="https://msdn.microsoft.com/dd9f5310-b1c0-46ff-b038-d6a50ac400a2">IAMTimecodeReader::SetTCRMode</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7fe74fc2-03bd-43dd-917f-ee0149f1e17f">IAMTimecodeGenerator Interface</a>
 

 

