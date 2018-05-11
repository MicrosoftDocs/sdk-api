---
UID: NF:sbe.IStreamBufferRecordingAttribute.EnumAttributes
title: IStreamBufferRecordingAttribute::EnumAttributes
author: windows-driver-content
description: The EnumAttributes method enumerates the existing attributes of the stream buffer file. This method returns an enumerator object, which the caller can then use to enumerate the attributes.
old-location: mstv\istreambufferrecordingattribute_enumattributes.htm
old-project: mstv
ms.assetid: 2944d1c4-a4ed-47a7-a0c4-a75cddb9cc99
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: EnumAttributes, EnumAttributes method [Microsoft TV Technologies], EnumAttributes method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],EnumAttributes method, IStreamBufferRecordingAttribute.EnumAttributes, IStreamBufferRecordingAttribute::EnumAttributes, IStreamBufferRecordingAttributeEnumAttributes, mstv.istreambufferrecordingattribute_enumattributes, sbe/IStreamBufferRecordingAttribute::EnumAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferRecordingAttribute.EnumAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStreamBufferRecordingAttribute::EnumAttributes


## -description


The <b>EnumAttributes</b> method enumerates the existing attributes of the stream buffer file. This method returns an enumerator object, which the caller can then use to enumerate the attributes.


## -parameters




### -param ppIEnumStreamBufferAttrib [out]

Receives an <a href="https://msdn.microsoft.com/668d2e04-74fa-41d7-b238-ec737a4441ca">IEnumStreamBufferRecordingAttrib</a> interface pointer.
          The caller must release the interface.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c46413f-3e51-4d72-b7f7-a8239c61b161">IStreamBufferRecordingAttribute Interface</a>
 

 

