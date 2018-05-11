---
UID: NF:sbe.IStreamBufferRecordingAttribute.GetAttributeByIndex
title: IStreamBufferRecordingAttribute::GetAttributeByIndex
author: windows-driver-content
description: The GetAttributeByIndex method retrieves an attribute, specified by index number.
old-location: mstv\istreambufferrecordingattribute_getattributebyindex.htm
old-project: mstv
ms.assetid: a4d9d25f-1e21-40e5-80c4-a8fe15dbc216
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetAttributeByIndex, GetAttributeByIndex method [Microsoft TV Technologies], GetAttributeByIndex method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],GetAttributeByIndex method, IStreamBufferRecordingAttribute.GetAttributeByIndex, IStreamBufferRecordingAttribute::GetAttributeByIndex, IStreamBufferRecordingAttributeGetAttributeByIndex, mstv.istreambufferrecordingattribute_getattributebyindex, sbe/IStreamBufferRecordingAttribute::GetAttributeByIndex
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
-	IStreamBufferRecordingAttribute.GetAttributeByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStreamBufferRecordingAttribute::GetAttributeByIndex


## -description


The <b>GetAttributeByIndex</b> method retrieves an attribute, specified by index number.


## -parameters




### -param wIndex [in]

Zero-based index of the attribute to retrieve.


### -param pulReserved [in]

Reserved. Set this parameter to zero.


### -param pszAttributeName [out]

Pointer to a buffer that receives the name of the attribute, as a null-terminated wide-character string. Specify the size of the buffer in the <i>pcchNameLength</i> parameter. To find out the required size for the array, set <i>pszAttributeName</i> to <b>NULL</b> and check the value that is returned in <i>pcchNameLength</i>.


### -param pcchNameLength [in, out]

On input, specifies the size of the buffer given in <i>pszAttributeName</i>, in wide characters. On output, contains the number of characters that were copied to the buffer, including the null terminator. Remember that wide characters are two bytes each.


### -param pStreamBufferAttributeType [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/be478769-d9ac-4e42-b5f6-94b5656e2596">STREAMBUFFER_ATTR_DATATYPE</a> enumeration. This value indicates the data type that you should use to interpret the attribute, which is returned in the <i>pbAttribute</i> parameter.


### -param pbAttribute [out]

Pointer to a buffer that receives the attribute, as an array of bytes. Specify the size of the buffer in the <i>pcbLength</i> parameter. To find out the required size for the array, set <i>pbAttribute</i> to <b>NULL</b> and check the value that is returned in <i>pcbLength</i>.


### -param pcbLength [in, out]

On input, specifies the size of the buffer given in <i>pbAttribute</i>, in bytes. On output, contains the number of bytes that were copied to the buffer.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
One or both of the buffers is too small.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c46413f-3e51-4d72-b7f7-a8239c61b161">IStreamBufferRecordingAttribute Interface</a>
 

 

