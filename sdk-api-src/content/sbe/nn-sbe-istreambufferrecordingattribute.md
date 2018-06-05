---
UID: NN:sbe.IStreamBufferRecordingAttribute
title: IStreamBufferRecordingAttribute
author: windows-sdk-content
description: The IStreamBufferRecordingAttribute interface sets and retrieves attributes on a stream buffer recording.
old-location: mstv\istreambufferrecordingattribute.htm
old-project: mstv
ms.assetid: 7c46413f-3e51-4d72-b7f7-a8239c61b161
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IStreamBufferRecordingAttribute, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies], IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],described, IStreamBufferRecordingAttributeInterface, mstv.istreambufferrecordingattribute, sbe/IStreamBufferRecordingAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferRecordingAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferRecordingAttribute interface


## -description



The <b>IStreamBufferRecordingAttribute</b> interface sets and retrieves attributes on a stream buffer recording. <i>Attributes</i> are metadata that describe the physical file (such as the bitrate and the duration) or the content of the file (such as the author or title).

This interface is exposed by the <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> object and the <a href="https://msdn.microsoft.com/dfb3e588-cf58-4f0f-a686-3aa7c7869247">RecordingAttributes</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecordingAttribute</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferRecordingAttribute</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2944d1c4-a4ed-47a7-a0c4-a75cddb9cc99">EnumAttributes</a>
</td>
<td align="left" width="63%">
Enumerates the existing attributes of the stream buffer file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4d9d25f-1e21-40e5-80c4-a8fe15dbc216">GetAttributeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute, specified by index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1191074-4ded-4e64-9c30-8e4d01390732">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Retrieves an attribute, specified by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ff4991-f6f2-4f70-bdf5-b8e1dc06611c">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Returns the number of attributes that are currently defined for this stream buffer file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc441a00-e98f-4ea7-b902-d74846fc93cc">SetAttribute</a>
</td>
<td align="left" width="63%">
Sets an attribute on the stream buffer file.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordingAttribute)</code>.




## -see-also




<a href="https://msdn.microsoft.com/6348884b-743b-45e3-b39d-a76c0fa12216">Stream Buffer Engine Attributes</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

