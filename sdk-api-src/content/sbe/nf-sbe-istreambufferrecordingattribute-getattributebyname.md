---
UID: NF:sbe.IStreamBufferRecordingAttribute.GetAttributeByName
title: IStreamBufferRecordingAttribute::GetAttributeByName (sbe.h)
description: The GetAttributeByName method retrieves an attribute, specified by name.
helpviewer_keywords: ["GetAttributeByName","GetAttributeByName method [Microsoft TV Technologies]","GetAttributeByName method [Microsoft TV Technologies]","IStreamBufferRecordingAttribute interface","IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","GetAttributeByName method","IStreamBufferRecordingAttribute.GetAttributeByName","IStreamBufferRecordingAttribute::GetAttributeByName","IStreamBufferRecordingAttributeGetAttributeByName","mstv.istreambufferrecordingattribute_getattributebyname","sbe/IStreamBufferRecordingAttribute::GetAttributeByName"]
old-location: mstv\istreambufferrecordingattribute_getattributebyname.htm
tech.root: mstv
ms.assetid: f1191074-4ded-4e64-9c30-8e4d01390732
ms.date: 12/05/2018
ms.keywords: GetAttributeByName, GetAttributeByName method [Microsoft TV Technologies], GetAttributeByName method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],GetAttributeByName method, IStreamBufferRecordingAttribute.GetAttributeByName, IStreamBufferRecordingAttribute::GetAttributeByName, IStreamBufferRecordingAttributeGetAttributeByName, mstv.istreambufferrecordingattribute_getattributebyname, sbe/IStreamBufferRecordingAttribute::GetAttributeByName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferRecordingAttribute::GetAttributeByName
 - sbe/IStreamBufferRecordingAttribute::GetAttributeByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecordingAttribute.GetAttributeByName
---

# IStreamBufferRecordingAttribute::GetAttributeByName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetAttributeByName</b> method retrieves an attribute, specified by name.

## -parameters

### -param pszAttributeName [in]

Wide-character string that contains the name of the attribute.

### -param pulReserved [in]

Reserved. Set this parameter to zero.

### -param pStreamBufferAttributeType [out]

Pointer to a variable that receives a member of the <a href="/previous-versions/windows/desktop/api/sbe/ne-sbe-streambuffer_attr_datatype">STREAMBUFFER_ATTR_DATATYPE</a> enumeration. This value indicates the data type that you should use to interpret the attribute, which is returned in the <i>pbAttribute</i> parameter.

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
The buffer given in <i>pbAttribute</i> is too small.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordingattribute">IStreamBufferRecordingAttribute Interface</a>