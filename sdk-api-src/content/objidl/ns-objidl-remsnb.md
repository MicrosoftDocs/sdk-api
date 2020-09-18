---
UID: NS:objidl.tagRemSNB
title: RemSNB (objidl.h)
description: The RemSNB structure is used for marshaling the SNB data type.Defined in the IStorage interface (Storag.idl).
helpviewer_keywords: ["*wireSNB","RemSNB","RemSNB structure [Structured Storage]","SNB","SNB structure pointer [Structured Storage]","_stg_remsnb","objidl/RemSNB","objidl/SNB","stg.remsnb"]
old-location: stg\remsnb.htm
tech.root: Stg
ms.assetid: 09a50518-2889-49ca-9d81-3035777ac2ac
ms.date: 12/05/2018
ms.keywords: '*wireSNB, RemSNB, RemSNB structure [Structured Storage], SNB, SNB structure pointer [Structured Storage], _stg_remsnb, objidl/RemSNB, objidl/SNB, stg.remsnb'
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RemSNB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRemSNB
 - objidl/tagRemSNB
 - RemSNB
 - objidl/RemSNB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - RemSNB
---

# RemSNB structure


## -description

The 
<b>RemSNB</b> structure is used for marshaling the 
<a href="/windows/desktop/Stg/snb">SNB</a> data type.

Defined in the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface (Storag.idl).

## -struct-fields

### -field ulCntStr

Number of strings in the <b>rgString</b> buffer.

### -field ulCntChar

Size in bytes of the <b>rgString</b> buffer.

### -field rgString

Pointer to an array of bytes containing the stream name strings from the <b>SNB</b> structure.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>