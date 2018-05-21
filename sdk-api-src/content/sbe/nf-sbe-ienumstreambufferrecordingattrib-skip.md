---
UID: NF:sbe.IEnumStreamBufferRecordingAttrib.Skip
title: IEnumStreamBufferRecordingAttrib::Skip
author: windows-driver-content
description: The Skip method skips over a specified number of attributes.
old-location: mstv\ienumstreambufferrecordingattrib_skip.htm
old-project: mstv
ms.assetid: 83beb8e9-f268-4ae1-a90b-548f0e3f6c99
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],Skip method, IEnumStreamBufferRecordingAttrib.Skip, IEnumStreamBufferRecordingAttrib::Skip, IEnumStreamBufferRecordingAttribSkip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],IEnumStreamBufferRecordingAttrib interface, mstv.ienumstreambufferrecordingattrib_skip, sbe/IEnumStreamBufferRecordingAttrib::Skip
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
-	IEnumStreamBufferRecordingAttrib.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumStreamBufferRecordingAttrib::Skip


## -description


The <b>Skip</b> method skips over a specified number of attributes.


## -parameters




### -param cRecords [in]

The number of attributes to skip.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped past the end of the sequence.

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
 




## -see-also




<a href="https://msdn.microsoft.com/668d2e04-74fa-41d7-b238-ec737a4441ca">IEnumStreamBufferRecordingAttrib Interface</a>
 

 

