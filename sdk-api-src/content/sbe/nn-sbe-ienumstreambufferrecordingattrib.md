---
UID: NN:sbe.IEnumStreamBufferRecordingAttrib
title: IEnumStreamBufferRecordingAttrib
author: windows-sdk-content
description: The IEnumStreamBufferRecordingAttrib interface enumerates a collection of attributes on a stream buffer file.
old-location: mstv\ienumstreambufferrecordingattrib.htm
old-project: mstv
ms.assetid: 668d2e04-74fa-41d7-b238-ec737a4441ca
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IEnumStreamBufferRecordingAttrib, IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies], IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],described, IEnumStreamBufferRecordingAttribInterface, mstv.ienumstreambufferrecordingattrib, sbe/IEnumStreamBufferRecordingAttrib
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IEnumStreamBufferRecordingAttrib
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IEnumStreamBufferRecordingAttrib interface


## -description



The <b>IEnumStreamBufferRecordingAttrib</b> interface enumerates a collection of attributes on a stream buffer file. <i>Attributes</i> are metadata that describe the physical file (such as the bit rate and the duration) or the content of the file (such as the author or title). To obtain this interface, call the <a href="https://msdn.microsoft.com/2944d1c4-a4ed-47a7-a0c4-a75cddb9cc99">IStreamBufferRecordingAttribute::EnumAttributes</a> method.

This interface implements a standard Component Object Model (COM) collection object. For more information on COM collections, see the <b>IEnumXXXX</b> topic in the Microsoft Platform SDK. The collection object represents a snapshot of the attributes when the collection is created; the collection is not updated automatically.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumStreamBufferRecordingAttrib</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumStreamBufferRecordingAttrib</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumStreamBufferRecordingAttrib</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of attributes in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of attributes.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumStreamBufferRecordingAttrib)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

