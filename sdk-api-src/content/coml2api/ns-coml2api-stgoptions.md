---
UID: NS:coml2api.tagSTGOPTIONS
title: STGOPTIONS (coml2api.h)
description: Specifies features of the storage object, such as sector size, in the StgCreateStorageEx and StgOpenStorageEx functions.
helpviewer_keywords: ["STGOPTIONS","STGOPTIONS structure [Structured Storage]","_stg_stgoptions","coml2api/STGOPTIONS","stg.stgoptions"]
old-location: stg\stgoptions.htm
tech.root: Stg
ms.assetid: dff6e626-d0c8-4b7c-85c7-c5cb2481d810
ms.date: 12/05/2018
ms.keywords: STGOPTIONS, STGOPTIONS structure [Structured Storage], _stg_stgoptions, coml2api/STGOPTIONS, stg.stgoptions
req.header: coml2api.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: STGOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTGOPTIONS
 - coml2api/tagSTGOPTIONS
 - STGOPTIONS
 - coml2api/STGOPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - coml2api.h
api_name:
 - STGOPTIONS
---

# STGOPTIONS structure


## -description

The 
<b>STGOPTIONS</b> structure specifies features of the storage object, such as sector size, in the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a> and 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex">StgOpenStorageEx</a> functions.

## -struct-fields

### -field usVersion

Specifies the version of the 
<b>STGOPTIONS</b> structure. It is set to <b>STGOPTIONS_VERSION</b>.

<div class="alert"><b>Note</b>  When  <b>usVersion</b> is set to 1, the <b>ulSectorSize</b> member can be set.  This is useful when creating a large-sector documentation file.  
However, when <b>usVersion</b> is set to 1, the <b>pwcsTemplateFile</b> member cannot be used.</div>
<div> </div>
<b>In Windows 2000 and later:  </b><b>STGOPTIONS_VERSION</b> can be set to 1 for version 1.

<b>In Windows XP and later:  </b><b>STGOPTIONS_VERSION</b> can be set to 2 for version 2.

<b>For operating systems prior to Windows 2000:  </b><b>STGOPTIONS_VERSION</b> will be set to 0 for version 0.

### -field reserved

Reserved for future use; must be zero.

### -field ulSectorSize

Specifies the sector size of the storage object. The default is 512 bytes.

### -field pwcsTemplateFile

Specifies the name of a file whose Encrypted File System (EFS) metadata will be transferred to a newly created Structured Storage file. This member is valid only when <b>STGFMT_DOCFILE</b> is used with <a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a>.

<b>In Windows XP and later:  </b>The <b>pwcsTemplateFile</b> member is only valid if version 2 or later is specified in the <b>usVersion</b> member.

## -remarks

<b>STGOPTIONS</b> is only supported on Unicode APIs.

## -see-also

<a href="/windows/desktop/Stg/structured-storage-interfaces">Compound File Implementation Limits</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex">StgOpenStorageEx</a>