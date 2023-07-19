---
UID: NS:sbe.STREAMBUFFER_ATTRIBUTE
title: STREAMBUFFER_ATTRIBUTE (sbe.h)
description: This topic applies only to Windows XP Service Pack 1 or later. The STREAMBUFFER_ATTRIBUTE structure describes an attribute on a stream buffer file.
helpviewer_keywords: ["STREAMBUFFER_ATTRIBUTE","STREAMBUFFER_ATTRIBUTE structure [Microsoft TV Technologies]","STREAMBUFFER_ATTRIBUTEStructure","mstv.streambuffer_attribute","sbe/STREAMBUFFER_ATTRIBUTE"]
old-location: mstv\streambuffer_attribute.htm
tech.root: mstv
ms.assetid: 2b17626a-9268-4192-8acf-ed46bf632163
ms.date: 12/05/2018
ms.keywords: STREAMBUFFER_ATTRIBUTE, STREAMBUFFER_ATTRIBUTE structure [Microsoft TV Technologies], STREAMBUFFER_ATTRIBUTEStructure, mstv.streambuffer_attribute, sbe/STREAMBUFFER_ATTRIBUTE
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: STREAMBUFFER_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - STREAMBUFFER_ATTRIBUTE
 - sbe/STREAMBUFFER_ATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sbe.h
api_name:
 - STREAMBUFFER_ATTRIBUTE
---

# STREAMBUFFER_ATTRIBUTE structure


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies only to Windows XP Service Pack 1 or later.
          

The <b>STREAMBUFFER_ATTRIBUTE</b> structure describes an attribute on a stream buffer file.

## -struct-fields

### -field pszName

Pointer to a null-terminated wide-character string that contains the name of the attribute.

### -field StreamBufferAttributeType

Member of the <a href="/previous-versions/windows/desktop/api/sbe/ne-sbe-streambuffer_attr_datatype">STREAMBUFFER_ATTR_DATATYPE</a> enumeration. The value indicates the data type that you should use to interpret the attribute data, which is contained in the <b>pbAttribute</b> member.

### -field pbAttribute

Pointer to a buffer that contains the attribute data.

### -field cbLength

The size of the buffer given in <b>pbAttribute</b>, in bytes.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-ienumstreambufferrecordingattrib-next">IEnumStreamBufferRecordingAttrib::Next</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-structures">Stream Buffer Engine Structures</a>