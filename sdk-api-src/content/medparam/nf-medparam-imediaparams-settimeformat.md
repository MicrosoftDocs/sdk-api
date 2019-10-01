---
UID: NF:medparam.IMediaParams.SetTimeFormat
title: IMediaParams::SetTimeFormat (medparam.h)
author: windows-sdk-content
description: The SetTimeFormat method specifies the time format for the object.
old-location: dshow\imediaparams_settimeformat.htm
tech.root: DirectShow
ms.assetid: 48c28dd8-aeae-4212-9221-ab943113aa76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaParams interface [DirectShow],SetTimeFormat method, IMediaParams.SetTimeFormat, IMediaParams::SetTimeFormat, IMediaParamsSetTimeFormat, SetTimeFormat, SetTimeFormat method [DirectShow], SetTimeFormat method [DirectShow],IMediaParams interface, dshow.imediaparams_settimeformat, medparam/IMediaParams::SetTimeFormat
ms.topic: method
f1_keywords: 
 - "medparam/IMediaParams.SetTimeFormat"
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParams.SetTimeFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaParams::SetTimeFormat


## -description



The <code>SetTimeFormat</code> method specifies the time format for the object.




## -parameters




### -param guidTimeFormat [in]

Time format GUID that specifies the time format.


### -param mpTimeData [in]

Value of type <b>MP_TIMEDATA</b> that specifies the unit of measure for the new format.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Object does not support this time format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



Objects can support more than one time format. Every object must support reference time, in which each unit of time is 100 nanoseconds (ns). Other formats are optional. The application must ensure that time stamps on the input buffers match whatever time format was set using this method.

The meaning of the <i>mpTimeData</i> parameter depends on the value of the <i>guidTimeFormat</i> parameter.

<table>
<tr>
<th>Time Format
            </th>
<th>Meaning of Time Data
            </th>
</tr>
<tr>
<td>GUID_TIME_MUSIC</td>
<td>Parts per quarter note.</td>
</tr>
<tr>
<td>GUID_TIME_REFERENCE</td>
<td>Ignored.</td>
</tr>
<tr>
<td>GUID_TIME_SAMPLES</td>
<td>Samples per second.</td>
</tr>
</table>
 

When you call this method, also call the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparams-flushenvelope">FlushEnvelope</a> method, to flush any envelopes that were set using the previous time format.

To determine what time formats an object supports, call the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat">IMediaParamInfo::GetSupportedTimeFormat</a> method. To retrieve the current format, call the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getcurrenttimeformat">IMediaParamInfo::GetCurrentTimeFormat</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>
 

 

