---
UID: NS:bits5_0.__MIDL___MIDL_itf_bits5_0_0000_0000_0002
title: BITS_FILE_PROPERTY_VALUE
description: Provides the property value of a BITS file.
helpviewer_keywords: ["BITS_FILE_PROPERTY_VALUE","BITS_FILE_PROPERTY_VALUE union [BITS]","bits.bits_file_property_value","bits5_0/BITS_FILE_PROPERTY_VALUE"]
old-location: bits\bits_file_property_value.htm
tech.root: Bits
ms.assetid: 0296014d-d5cc-40f0-a3d3-93d8ea704ce5
ms.date: 12/05/2018
ms.keywords: BITS_FILE_PROPERTY_VALUE, BITS_FILE_PROPERTY_VALUE union [BITS], bits.bits_file_property_value, bits5_0/BITS_FILE_PROPERTY_VALUE
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BITS_FILE_PROPERTY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_bits5_0_0000_0000_0002
 - bits5_0/__MIDL___MIDL_itf_bits5_0_0000_0000_0002
 - BITS_FILE_PROPERTY_VALUE
 - bits5_0/BITS_FILE_PROPERTY_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits5_0.h
api_name:
 - BITS_FILE_PROPERTY_VALUE
---

## -description

Provides the property value of the BITS file based on a value from the <a href="/windows/desktop/api/bits5_0/ns-bits5_0-bits_job_property_value">BITS_FILE_PROPERTY_ID</a> enumeration.

## -struct-fields

### -field String

This value is used when using the property ID 
      enum value <b>BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS</b>.

## -see-also

<a href="/windows/desktop/api/bits5_0/ns-bits5_0-bits_job_property_value">BITS_FILE_PROPERTY_ID</a>



<a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-getproperty">IBackgroundCopyFile5.GetProperty</a>



<a href="/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-setproperty">IBackgroundCopyFile5.SetProperty</a>