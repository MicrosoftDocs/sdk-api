---
UID: NF:sbe.IEnumStreamBufferRecordingAttrib.Next
title: IEnumStreamBufferRecordingAttrib::Next
author: windows-sdk-content
description: The Next method returns a specified number of attributes in the enumeration sequence.
old-location: mstv\ienumstreambufferrecordingattrib_next.htm
old-project: mstv
ms.assetid: 760b2e2c-799d-45e5-9dbd-2407e7431918
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],Next method, IEnumStreamBufferRecordingAttrib.Next, IEnumStreamBufferRecordingAttrib::Next, IEnumStreamBufferRecordingAttribNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumStreamBufferRecordingAttrib interface, mstv.ienumstreambufferrecordingattrib_next, sbe/IEnumStreamBufferRecordingAttrib::Next
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumStreamBufferRecordingAttrib.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IEnumStreamBufferRecordingAttrib::Next


## -description


The <b>Next</b> method returns a specified number of attributes in the enumeration sequence.


## -parameters




### -param cRequest [in]

The number of attributes to retrieve.


### -param pStreamBufferAttribute [in, out]

Pointer to an array of size <i>cRequest</i>. The array is filled with <a href="https://msdn.microsoft.com/2b17626a-9268-4192-8acf-ed46bf632163">STREAMBUFFER_ATTRIBUTE</a> structures.


### -param pcReceived [out]

Pointer to a variable that receives the number of attributes that are returned in the <i>pStreamBufferAttribute</i> array. This parameter can be <b>NULL</b> if <i>cRequest</i> is 1.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Did not retrieve as many attributes as requested (reached the end of the enumeration).

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
 




## -remarks



The caller allocates the array of <a href="https://msdn.microsoft.com/2b17626a-9268-4192-8acf-ed46bf632163">STREAMBUFFER_ATTRIBUTE</a> structures, but the method allocates buffers for the attributes and the attribute names, which are contained in the <b>pszName</b> and <b>pbAttribute</b> members of each structure. The caller must release those buffers, by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/668d2e04-74fa-41d7-b238-ec737a4441ca">IEnumStreamBufferRecordingAttrib Interface</a>
 

 

