---
UID: NS:msctf.TF_PERSISTENT_PROPERTY_HEADER_ACP
title: TF_PERSISTENT_PROPERTY_HEADER_ACP (msctf.h)
description: The TF_PERSISTENT_PROPERTY_HEADER_ACP structure is used to provide property header data.
helpviewer_keywords: ["TF_PERSISTENT_PROPERTY_HEADER_ACP","TF_PERSISTENT_PROPERTY_HEADER_ACP structure [Text Services Framework]","_tsf_tf_persistent_property_header_acp_ref","msctf/TF_PERSISTENT_PROPERTY_HEADER_ACP","tsf.tf_persistent_property_header_acp"]
old-location: tsf\tf_persistent_property_header_acp.htm
tech.root: TSF
ms.assetid: 9c5cb193-d18e-4d91-b9be-b8a61a56d3a3
ms.date: 12/05/2018
ms.keywords: TF_PERSISTENT_PROPERTY_HEADER_ACP, TF_PERSISTENT_PROPERTY_HEADER_ACP structure [Text Services Framework], _tsf_tf_persistent_property_header_acp_ref, msctf/TF_PERSISTENT_PROPERTY_HEADER_ACP, tsf.tf_persistent_property_header_acp
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TF_PERSISTENT_PROPERTY_HEADER_ACP
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_PERSISTENT_PROPERTY_HEADER_ACP
 - msctf/TF_PERSISTENT_PROPERTY_HEADER_ACP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_PERSISTENT_PROPERTY_HEADER_ACP
---

# TF_PERSISTENT_PROPERTY_HEADER_ACP structure


## -description

The <b>TF_PERSISTENT_PROPERTY_HEADER_ACP</b> structure is used to provide property header data.

## -struct-fields

### -field guidType

Contains a GUID that identifies the property.

### -field ichStart

Contains the starting character position of the property.

### -field cch

Contains the number of characters that the property spans.

### -field cb

Contains the size, in bytes, of the property value.

### -field dwPrivate

Contains a <b>DWORD</b> value defined by the property owner.

### -field clsidTIP

Contains the CLSID of the property owner.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize">ITextStoreACPServices::Serialize
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-serialize">ITfContextOwnerServices::Serialize
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextownerservices-unserialize">ITfContextOwnerServices::Unserialize
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfpersistentpropertyloaderacp-loadproperty">ITfPersistentPropertyLoaderACP::LoadProperty
      </a>