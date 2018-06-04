---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# acmMetrics function


## -description



The <b>acmMetrics</b> function returns various metrics for the ACM or related ACM objects.




## -parameters




### -param hao

Handle to the ACM object to query for the metric specified in <i>uMetric</i>. For some queries, this parameter can be <b>NULL</b>.


### -param uMetric

Metric index to be returned in <i>pMetric</i>.

<table>
<tr>
<th>
Value
</th>
<th>
Meaning
</th>
</tr>
<tr>
<td>ACM_METRIC_COUNT_CODECS</td>
<td>Returned value is the number of global ACM compressor or decompressor drivers in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_CONVERTERS</td>
<td>Returned value is the number of global ACM converter drivers in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_DISABLED</td>
<td>Returned value is the total number of global disabled ACM drivers (of all support types) in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value. The sum of the ACM_METRIC_COUNT_DRIVERS and ACM_METRIC_COUNT_DISABLED metric indices is the total number of globally installed ACM drivers.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_DRIVERS</td>
<td>Returned value is the total number of enabled global ACM drivers (of all support types) in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_FILTERS</td>
<td>Returned value is the number of global ACM filter drivers in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_HARDWARE</td>
<td>Returned value is the number of global ACM hardware drivers in the system. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_LOCAL_CODECS</td>
<td>Returned value is the number of local ACM compressor drivers, ACM decompressor drivers, or both for the calling task. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_LOCAL_CONVERTERS</td>
<td>Returned value is the number of local ACM converter drivers for the calling task. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_LOCAL_DISABLED</td>
<td>Returned value is the total number of local disabled ACM drivers, of all support types, for the calling task. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value. The sum of the ACM_METRIC_COUNT_LOCAL_DRIVERS and ACM_METRIC_COUNT_LOCAL_DISABLED metric indices is the total number of locally installed ACM drivers.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_LOCAL_DRIVERS</td>
<td>Returned value is the total number of enabled local ACM drivers (of all support types) for the calling task. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_COUNT_LOCAL_FILTERS</td>
<td>Returned value is the number of local ACM filter drivers for the calling task. The <i>hao</i> parameter must be <b>NULL</b> for this metric index. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_DRIVER_PRIORITY</td>
<td>Returned value is the current priority for the specified driver. The <i>hao</i> parameter must be a valid ACM driver identifier of the <b>HACMDRIVERID</b> data type. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_DRIVER_SUPPORT</td>
<td>Returned value is the <b>fdwSupport</b> flags for the specified driver. The <i>hao</i> parameter must be a valid ACM driver identifier of the <b>HACMDRIVERID</b> data type. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_HARDWARE_WAVE_INPUT</td>
<td>Returned value is the waveform-audio input device identifier associated with the specified driver. The <i>hao</i> parameter must be a valid ACM driver identifier of the <b>HACMDRIVERID</b> data type that supports the ACMDRIVERDETAILS_SUPPORTF_HARDWARE flag. If no waveform-audio input device is associated with the driver, MMSYSERR_NOTSUPPORTED is returned. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_HARDWARE_WAVE_OUTPUT</td>
<td>Returned value is the waveform-audio output device identifier associated with the specified driver. The <i>hao</i> parameter must be a valid ACM driver identifier of the <b>HACMDRIVERID</b> data type that supports the ACMDRIVERDETAILS_SUPPORTF_HARDWARE flag. If no waveform-audio output device is associated with the driver, MMSYSERR_NOTSUPPORTED is returned. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value.</td>
</tr>
<tr>
<td>ACM_METRIC_MAX_SIZE_FILTER</td>
<td>Returned value is the size of the largest <a href="https://msdn.microsoft.com/dea3df47-88a2-439f-bf07-b5c592bf23e8">WAVEFILTER</a> structure. If <i>hao</i> is <b>NULL</b>, the return value is the largest <b>WAVEFILTER</b> structure in the system. If <i>hao</i> identifies an open instance of an ACM driver of the <b>HACMDRIVER</b> data type or an ACM driver identifier of the <b>HACMDRIVERID</b> data type, the largest <b>WAVEFILTER</b> structure for that driver is returned. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value. This metric is not allowed for an ACM stream handle of the <b>HACMSTREAM</b> data type.</td>
</tr>
<tr>
<td>ACM_METRIC_MAX_SIZE_FORMAT</td>
<td>Returned value is the size of the largest <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure. If <i>hao</i> is <b>NULL</b>, the return value is the largest <b>WAVEFORMATEX</b> structure in the system. If <i>hao</i> identifies an open instance of an ACM driver of the <b>HACMDRIVER</b> data type or an ACM driver identifier of the <b>HACMDRIVERID</b> data type, the largest <b>WAVEFORMATEX</b> structure for that driver is returned. The <i>pMetric</i> parameter must point to a buffer of a size equal to a <b>DWORD</b> value. This metric is not allowed for an ACM stream handle of the <b>HACMSTREAM</b> data type.</td>
</tr>
</table>
 


### -param pMetric

Pointer to the buffer to receive the metric details. The exact definition depends on the <i>uMetric</i> index.


## -returns



Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The index specified in <i>uMetric</i> cannot be returned for the specified <i>hao</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The index specified in <i>uMetric</i> is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

