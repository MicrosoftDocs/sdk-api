---
UID: NF:winevt.EvtGetEventMetadataProperty
title: EvtGetEventMetadataProperty function
author: windows-sdk-content
description: Gets the specified event metadata property.
old-location: wes\evtgeteventmetadataproperty.htm
tech.root: WES
ms.assetid: 2a5c53e3-bbb4-4245-a640-86b58d1a3c52
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: EvtGetEventMetadataProperty, EvtGetEventMetadataProperty function [EventLog], wes.evtgeteventmetadataproperty, winevt/EvtGetEventMetadataProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winevt.h
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtGetEventMetadataProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetEventMetadataProperty function


## -description


Gets the specified event metadata property.


## -parameters




### -param EventMetadata [in]

A handle to the event metadata that the  <a href="https://msdn.microsoft.com/1077dc7c-3e73-4135-9020-20d086e30e71">EvtNextEventMetadata</a> function returns.


### -param PropertyId [in]

The identifier of the metadata property to retrieve. For a list of property identifiers, see the <a href="https://msdn.microsoft.com/d5a71e51-c080-4976-9f33-fe24b523ae81">EVT_EVENT_METADATA_PROPERTY_ID</a> enumeration.


### -param Flags [in]

Reserved. Must be zero.


### -param EventMetadataPropertyBufferSize [in]

The size of the <i>EventMetadataPropertyBuffer</i> buffer, in bytes.


### -param EventMetadataPropertyBuffer [in]

A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


### -param EventMetadataPropertyBufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>



<a href="https://msdn.microsoft.com/1077dc7c-3e73-4135-9020-20d086e30e71">EvtNextEventMetadata</a>
 

 

