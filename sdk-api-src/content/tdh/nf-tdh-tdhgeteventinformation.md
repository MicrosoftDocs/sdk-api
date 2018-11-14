---
UID: NF:tdh.TdhGetEventInformation
title: TdhGetEventInformation function
author: windows-sdk-content
description: Retrieves metadata about an event.
old-location: etw\tdhgeteventinformation_func.htm
tech.root: etw
ms.assetid: 81542550-79aa-4d67-a472-ac3ee3a3ce63
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TdhGetEventInformation, TdhGetEventInformation function [ETW], etw.tdhgeteventinformation_func, tdh.tdhgeteventinformation_func, tdh/TdhGetEventInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhGetEventInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TdhGetEventInformation
: 
---

# TdhGetEventInformation function


## -description


Retrieves metadata about an event.


## -parameters




### -param Event [in]

The event record passed to your <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback. For details, see the <a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a> structure.


### -param TdhContextCount [in]

Number of elements in <i>pTdhContext</i>.


### -param TdhContext [in]

Array of context values for WPP or classic ETW events only; otherwise, <b>NULL</b>. For details, see the <a href="https://msdn.microsoft.com/184df0af-3ac5-406f-a298-4f23826ad85e">TDH_CONTEXT</a> structure.  The array must not contain duplicate context types.


### -param Buffer [out]

User-allocated buffer to receive the event information. For details, see the <a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a> structure.


### -param BufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pBuffer</i> buffer is too small. Use the required buffer size set in <i>pBufferSize</i> to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema for the event was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>resourceFileName</b> attribute in the manifest contains the location of the provider binary. When you register the manifest, the location is written to the registry. TDH was unable to find the binary based on the registered location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The WMI service is not available.

</td>
</tr>
</table>
 




## -remarks



If the event is a WPP or legacy ETW event, you can specify context information that is used to help parse the event information. The event is a WPP event if the EVENT_HEADER_FLAG_TRACE_MESSAGE flag is set in the <b>Flags</b> member of <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> (see the <b>EventHeader</b> member of <a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>). The event is a legacy ETW event if the EVENT_HEADER_FLAG_CLASSIC_HEADER flag is set.


#### Examples

For an example that shows how to retrieve metadata about an event, see <a href="https://msdn.microsoft.com/5ebd500c-420e-4979-a03a-49b687464b0e">Using TdhFormatProperty to Consume Event Data</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2625b65c-7f9e-4a87-85c6-d16857ef4987">TdhGetEventMapInformation</a>



<a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a>
 

 

