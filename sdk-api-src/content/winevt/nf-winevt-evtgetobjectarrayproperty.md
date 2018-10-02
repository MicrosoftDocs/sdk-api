---
UID: NF:winevt.EvtGetObjectArrayProperty
title: EvtGetObjectArrayProperty function
author: windows-sdk-content
description: Gets a provider metadata property from the specified object in the array.
old-location: wes\evtgetobjectarrayproperty.htm
tech.root: WES
ms.assetid: a522f0a8-6050-4082-acdf-e700ebfa7efc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EvtGetObjectArrayProperty, EvtGetObjectArrayProperty function [EventLog], wes.evtgetobjectarrayproperty, winevt/EvtGetObjectArrayProperty
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
 - EvtGetObjectArrayProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtGetObjectArrayProperty function


## -description


Gets a provider metadata property from the specified object in the array.


## -parameters




### -param ObjectArray [in]

A handle to an array of objects that the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a> function returns.


### -param PropertyId [in]

The property identifier of the metadata property that you want to get from the  specified object. For possible values, see the Remarks section of <a href="https://msdn.microsoft.com/10f4917d-68a1-4e90-ad7f-6bc19471ec38">EVT_PUBLISHER_METADATA_PROPERTY_ID</a>.


### -param ArrayIndex [in]

The zero-based index of the object in the array.


### -param Flags [in]

Reserved. Must be zero.


### -param PropertyValueBufferSize [in]

The size of the <i>PropertyValueBuffer</i> buffer, in bytes.


### -param PropertyValueBuffer [in]

A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


### -param PropertyValueBufferUsed [out]

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
 




## -remarks



When you call the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a> function with the following IDs, the function returns a handle to an array of objects of that type:

<ul>
<li>EvtPublisherMetadataChannelReferences</li>
<li>EvtPublisherMetadataLevels</li>
<li>EvtPublisherMetadataTasks</li>
<li>EvtPublisherMetadataOpcodes</li>
<li>EvtPublisherMetadataKeywords</li>
</ul>
For example, if you pass <b>EvtPublisherMetadataKeywords</b> to <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>, the function returns a handle to an array of keyword objects.

To determine the size of the array, call the <a href="https://msdn.microsoft.com/fc4043ac-48eb-400b-8cf6-b83cbbb2765c">EvtGetObjectArraySize</a> function.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/10f4917d-68a1-4e90-ad7f-6bc19471ec38">EVT_PUBLISHER_METADATA_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>
 

 

