---
UID: NF:sbe.IStreamBufferRecordingAttribute.SetAttribute
title: IStreamBufferRecordingAttribute::SetAttribute (sbe.h)
description: The SetAttribute method sets an attribute on the stream buffer file.
helpviewer_keywords: ["IStreamBufferRecordingAttribute interface [Microsoft TV Technologies]","SetAttribute method","IStreamBufferRecordingAttribute.SetAttribute","IStreamBufferRecordingAttribute::SetAttribute","IStreamBufferRecordingAttributeSetAttribute","SetAttribute","SetAttribute method [Microsoft TV Technologies]","SetAttribute method [Microsoft TV Technologies]","IStreamBufferRecordingAttribute interface","mstv.istreambufferrecordingattribute_setattribute","sbe/IStreamBufferRecordingAttribute::SetAttribute"]
old-location: mstv\istreambufferrecordingattribute_setattribute.htm
tech.root: mstv
ms.assetid: cc441a00-e98f-4ea7-b902-d74846fc93cc
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordingAttribute interface [Microsoft TV Technologies],SetAttribute method, IStreamBufferRecordingAttribute.SetAttribute, IStreamBufferRecordingAttribute::SetAttribute, IStreamBufferRecordingAttributeSetAttribute, SetAttribute, SetAttribute method [Microsoft TV Technologies], SetAttribute method [Microsoft TV Technologies],IStreamBufferRecordingAttribute interface, mstv.istreambufferrecordingattribute_setattribute, sbe/IStreamBufferRecordingAttribute::SetAttribute
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
 - IStreamBufferRecordingAttribute::SetAttribute
 - sbe/IStreamBufferRecordingAttribute::SetAttribute
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
 - IStreamBufferRecordingAttribute.SetAttribute
---

# IStreamBufferRecordingAttribute::SetAttribute


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetAttribute</b> method sets an attribute on the stream buffer file.

## -parameters

### -param ulReserved [in]

Reserved. Set this parameter to zero.

### -param pszAttributeName [in]

Wide-character string that contains the name of the attribute.

### -param StreamBufferAttributeType [in]

Member of the <a href="/previous-versions/windows/desktop/api/sbe/ne-sbe-streambuffer_attr_datatype">STREAMBUFFER_ATTR_DATATYPE</a> enumeration that defines the data type of the attribute data.

### -param pbAttribute [in]

Pointer to a buffer that contains the attribute data.

### -param cbAttributeLength [in]

The size of the buffer specified in <i>pbAttribute</i>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

If an attribute with that name already exists, the method overwrites it with the new value.

The method fails if the recorder object is already recording.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">IStreamBufferRecordControl::Start</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordingattribute">IStreamBufferRecordingAttribute Interface</a>