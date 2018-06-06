---
UID: NF:winevt.EvtGetPublisherMetadataProperty
title: EvtGetPublisherMetadataProperty function
author: windows-sdk-content
description: Gets the specified provider metadata property.
old-location: wes\evtgetpublishermetadataproperty.htm
old-project: WES
ms.assetid: f85a46ef-873c-4dd9-8b5c-3763fd67fc06
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EvtGetPublisherMetadataProperty, EvtGetPublisherMetadataProperty function [EventLog], wes.evtgetpublishermetadataproperty, winevt/EvtGetPublisherMetadataProperty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtGetPublisherMetadataProperty
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtGetPublisherMetadataProperty function


## -description


Gets the specified provider metadata property.


## -parameters




### -param PublisherMetadata [in]

A handle to the metadata that the  <a href="https://msdn.microsoft.com/0839fb15-12a9-4e30-9afa-6f6437956df0">EvtOpenPublisherMetadata</a> function returns.


### -param PropertyId [in]

The identifier of the metadata property to retrieve. For a list of property identifiers, see the <a href="https://msdn.microsoft.com/10f4917d-68a1-4e90-ad7f-6bc19471ec38">EVT_PUBLISHER_METADATA_PROPERTY_ID</a> enumeration.


### -param Flags [in]

Reserved. Must be zero.


### -param PublisherMetadataPropertyBufferSize [in]

The size of the <i>PublisherMetadataPropertyBuffer</i> buffer, in bytes.


### -param PublisherMetadataPropertyBuffer [in]


A caller-allocated buffer that will receive the metadata property. The buffer contains an <a href="https://msdn.microsoft.com/4b0f338b-0b66-4ba5-9e29-b15afe15a2d3">EVT_VARIANT</a> object. You can set this parameter to <b>NULL</b> to determine the required buffer size.


### -param PublisherMetadataPropertyBufferUsed [out]

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



<div class="alert"><b>Caution</b>  <p class="note">
<a href="https://msdn.microsoft.com/2a5c53e3-bbb4-4245-a640-86b58d1a3c52">EvtGetEventMetadataProperty</a> can return many different kinds of values in the <i>EventMetadataPropertyBuffer</i> variable. If <i>EventMetadataPropertyBuffer</i>-&gt;Type == <b>EvtVarTypeEvtHandle</b> then <i>EventMetadataPropertyBuffer</i> contains a handle that needs to be freed. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function. 

</div>
<div> </div>

#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0839fb15-12a9-4e30-9afa-6f6437956df0">EvtOpenPublisherMetadata</a>
 

 

