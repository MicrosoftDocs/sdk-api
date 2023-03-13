---
UID: NE:objidl.tagDATADIR
title: DATADIR (objidl.h)
description: Specifies the direction of the data flow. This determines the formats that the resulting enumerator can enumerate.
helpviewer_keywords: ["DATADIR","DATADIR enumeration [COM]","DATADIR_GET","DATADIR_SET","_ole_DATADIR","com.datadir","objidl/DATADIR","objidl/DATADIR_GET","objidl/DATADIR_SET"]
old-location: com\datadir.htm
tech.root: com
ms.assetid: 395d7511-f491-4d6c-9360-cae7e16e8524
ms.date: 12/05/2018
ms.keywords: DATADIR, DATADIR enumeration [COM], DATADIR_GET, DATADIR_SET, _ole_DATADIR, com.datadir, objidl/DATADIR, objidl/DATADIR_GET, objidl/DATADIR_SET
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
req.typenames: DATADIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDATADIR
 - objidl/tagDATADIR
 - DATADIR
 - objidl/DATADIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - DATADIR
---

# DATADIR enumeration


## -description

Specifies the direction of the data flow. This determines the formats that the resulting enumerator can enumerate.

## -enum-fields

### -field DATADIR_GET:1

Requests that <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>.

### -field DATADIR_SET:2

Requests that <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>
