---
UID: NN:sbe.IStreamBufferRecordingAttribute
title: IStreamBufferRecordingAttribute (sbe.h)
author: windows-sdk-content
description: The IStreamBufferRecordingAttribute interface sets and retrieves attributes on a stream buffer recording.
old-location: mstv\istreambufferrecordingattribute.htm
tech.root: mstv
ms.assetid: 7c46413f-3e51-4d72-b7f7-a8239c61b161
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordingAttribute, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies], IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],described, IStreamBufferRecordingAttributeInterface, mstv.istreambufferrecordingattribute, sbe/IStreamBufferRecordingAttribute
ms.topic: interface
f1_keywords: 
 - "sbe/IStreamBufferRecordingAttribute"
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecordingAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferRecordingAttribute interface


## -description



The <b>IStreamBufferRecordingAttribute</b> interface sets and retrieves attributes on a stream buffer recording. <i>Attributes</i> are metadata that describe the physical file (such as the bitrate and the duration) or the content of the file (such as the author or title).

This interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/recording-object">Recording</a> object and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/recordingattributes-object">RecordingAttributes</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecordingAttribute</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecordingAttribute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferRecordingAttribute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-enumattributes">EnumAttributes</a>
</td>
<td align="left" width="63%">
Enumerates the existing attributes of the stream buffer file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd377126(v=vs.85)">GetAttributeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute, specified by index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-getattributebyname">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Retrieves an attribute, specified by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-getattributecount">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Returns the number of attributes that are currently defined for this stream buffer file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-setattribute">SetAttribute</a>
</td>
<td align="left" width="63%">
Sets an attribute on the stream buffer file.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordingAttribute)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-attributes">Stream Buffer Engine Attributes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

